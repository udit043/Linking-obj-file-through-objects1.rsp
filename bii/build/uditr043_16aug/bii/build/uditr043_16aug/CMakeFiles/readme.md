When you want to link any .obj/.o file in biicode then according to guide (http://docs.biicode.com/c++/adapt_library_guide.html)
You have to make changes in CMakeList.txt but i found another way to link object file.
#example
Here i use conio.o , an object file and i want to link this object file in my program (main.c)
Instead of editing CMakeList.txt i edit objects1.rsp file inside 
(bii/build/uditr043_16aug/CMakeFiles/uditr043_16aug_main.dir) folder.

I just add one line to it and programs runs withous any linker error

Previously objects1.rsp was : CMakeFiles/uditr043_16aug_main.dir/main.cpp.obj
But this gives linker error : undefined reference to 'textcolor'

objects1.rsp after editing : CMakeFiles/uditr043_16aug_main.dir/main.cpp.obj CMakeFiles/uditr043_16aug_main.dir/conio.o
After adding this one line ("CMakeFiles/uditr043_16aug_main.dir/conio.o") programs runs fine.

Is this a bug ? 
