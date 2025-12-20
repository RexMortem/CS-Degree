(This is a very rough document that will basically only be helpful for me)
## Things important for the essay 

- Good academic references
- Good summary/evaluation of the main references

- Personal flair and personal experience in Lua
## Choice of Language and Publications Blog Post

Lua started as a "glue" language designed to integrate well with software written in C and other more established languages

[1] R. Ierusalimschy, L. H. de Figueiredo, and W. Celes, “The evolution of Lua,” _Proceedings of the third ACM SIGPLAN conference on History of programming languages_, Jun. 2007, doi: https://doi.org/10.1145/1238844.1238846.

[2] R. Ierusalimschy and Lablua, _Programming in Lua_. Rio De Janeiro: Lua.org, 2016.

[3] R. Ierusalimschy, L. H. De Figueiredo, and W. Celes, “A look at the design of Lua,” _Communications of the ACM_, vol. 61, no. 11, pp. 114–123, Oct. 2018, doi: https://doi.org/10.1145/3186277.
## Key Features for game development

- Want decent performance (don't need amazing performance though if the engine is implemented in a different language) -> can contrast against another scripting language Python which is way slower
	- although performance is hard to benchmark
- Want to be able to do event-driven architecture and basic OOP (or do you?)
- Incredible iteration speed and prototyping 

- Simplicity -> can we find references suggesting that Python/Java/C++ are more complicated? 

- Modularity -> first-class functions 
## Key Points

- Dynamic typing is a counterpoint here - the dynamic typing in Lua arguably makes it less suited for huge codebases and reliable code design (mention typed Lua in ROBLOX)


## Event-Driven Architecture 

```Lua
-- naturally use metatables here
local EventfulObject = {}
EventfulObject.__index = EventfulObject 

function EventfulObject.new()
  return setmetatable({
    Events = {}
  }, EventfulObject)
end

-- using variadic functions here
function EventfulObject:FireEvent(EventName, ...)
  if self.Events[EventName] then
    for _, CallbackFunction in ipairs(self.Events[EventName]) do
      CallbackFunction(...)
    end
  else
    warn("No event with the name '" .. EventName .. "'!")
  end
end

function EventfulObject:Connect(EventName, CallbackFunction)
  if not self.Events[EventName] then
    self.Events[EventName] = {}
  end
  
  table.insert(self.Events[EventName], CallbackFunction)
end

local obj1 = EventfulObject.new()

obj1:Connect("InflictDamage", function(dmg)
  print("some damage: " .. dmg)
end)

obj1:FireEvent("InflictDamage", 25)
obj1:FireEvent("InflictDamage", 50)
```


The choice to have tables as a primitive type sets the stage for tables being a core part of the language - indeed, anything interesting in the language (e.g. data structures such as queues) will be represented with tables. 