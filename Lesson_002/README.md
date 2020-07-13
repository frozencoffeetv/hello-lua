# Chunks 

In Lua, a chunk is a sequence of statements. 

*It could be a file or single line of code in interactive mode*

You can pass arguments to a lua script either before or after the script itself

```sh
lua -e "a = 5" args.lua --watch --prod --force 
```

Will print the following...

```sh
-3      lua
-2      -e
-1      a = 5
0       args.lua
1       --watch
2       --prod
3       --force
```

the script name is always at index 0 of the generated *arg* table. arguments that pertain to the lua cli and thus come before the script are at indicies proceeding 0, and arguments that follow the script increment after 0.