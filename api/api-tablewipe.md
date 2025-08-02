# API table.wipe

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
'''Wipes''' a table of all contents.
 table = table.wipe(table)
 wipe(table)

==Arguments==
:;table:{{apitype|table}} - The table to be cleared.

==Returns==
:;table:{{apitype|table}} - The empty table.

==Example==
 local tab = {}
 tab.Hello = "Goodbye"
 print(tab.Hello) -- print "Goodbye"
 tab = table.wipe(tab)
 print(tab.Hello) -- print nil

==Details==
* While this function returns an empty table, it is not necessary to assign it to a variable.

 local t = {"stuff"}
 t = wipe(t)
 print(#t) -- prints 0
 
 local t = {"stuff"}
 wipe(t)
 print(#t) -- also prints 0

* The difference between ''wipe(table)'' and ''table={}'' is that ''wipe'' removes the contents of the table, but retains the variable's internal pointer.

 data={1,2,3}
 
 copy=data
 assert(copy==data)   -- they're the same object
 copy={}
 assert(copy~=data)   -- they're no longer the same:
 assert(#copy==0)     -- the copy is expectedly empty,
 assert(#data==3)     -- but the original table remains.
 
 copy2=data
 assert(copy2==data)  -- they're the same object
 wipe(copy2)
 assert(copy2==data)  -- they're still the same object:
 assert(#copy2==0)    -- the copy is expectedly empty,
 assert(#data==0)     -- and so is the original table.

* ''wipe(table)'' preserves any metatable set to ''table''.

 table={1,2,3}
 meta={__index={["foo"]="bar"}}
 setmetatable(table,meta)
 
 print(table["foo"])-- prints "bar"
 wipe(table)
 print(table["foo"])-- still prints "bar"
```