I've read so many times that Reason compiled not only to JavaScript, but to bytecode as well. So, I decided to learn how to do that.

I used ``bsb-native`` which is a fork of `bsb` build system that use BuckleScript to compile Reason to JS. Since ``bsb-native`` is ``bsb`` fork,it contains original BuckleScript (``bsc``) with added bytecode (``ocamlc``) and native (``ocamlopt``).  

Both ``bsb`` and ``bsb-native`` are simple build systems, coordinating calls to the compilers.

I created new a Reason project using  
 ``bsb -init my-first-app -theme basic-reason``.  
 Then I modified ``bsconfig.json`` file by changing the devDependecy 
 ``bs-platform": "bsansouci/bsb-native#2.1.1``
 and added ``entries`` property.

 Then I wrote my Reason code to ``Index.re`` and run the build command that compiled my code to bytecode and I saw ``hello world`` output in the console 🎉.

```reason
print_endline("Hello world")
```

