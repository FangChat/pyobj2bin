# pyobj2bin
This module can be used to store python objects in binary format and only has one error class : FileObjectError. 

Functions: 
1. dump(): 
The dump functions needs two arguments (the python object and file handler object) 

Usage: 
      pyobj2bin.dump(o,f) 
      where o is the python object and f is the file handler object 

2. load(): 
The load function loads all the data stored in the file and returns a list containing all the python objects 

Usage: 
      pyobj2bin.load(f) 
      where f is the file handler object 

3. showtype(): 
The showtype module returns a list containing the data types of all the objects stored in the binary file 

Usage: 
      pyobj2bin.showtype(f) 
      where f is the file handler object 

4. update(): The update function displays all the different objects stored in the file and you can choose one of the existing object and enter a new value(this will be passed as an object that replaces the existing object) 

Usage: 
      pyobj2bin.update(f) 
      where f is the file handler object 

5. load_module(): The load_module function is useful when you want to create an object using other modules and store it in the binary file. This function will load the specified module as a part of the pyobj2bin module instead of importing it in the main program and it evaluates the object automatically while storing it in the binary file 

Usage: 
      eg: 
         pyobj2bin.load_module("datetime") 
         [[1, 2, 3], [1, 2, 3]] 
         Which object do you want to update: 
         1. [1, 2, 3] 
         2. [1, 2, 3] 
         Enter your choice: 2 
         Enter new value: datetime.datetime(2022,10,10) 
         [[1, 2, 3], '2022-10-10 00:00:00'] 

         Here you can see that the value of datetime.datetime(2022,10,10) was evaluated and stored in the file 

         Note: If you do not use the load_module function the module will store the object as a string. 
         For example here if we did not use the function, the output would be: 

         [[1, 2, 3], [1, 2, 3]] 
         Which object do you want to update: 
         1. [1, 2, 3] 
         2. [1, 2, 3] 
         Enter your choice: 2 
         Enter new value: datetime.datetime(2022,10,10) 
         [[1, 2, 3], 'datetime.datetime(2022,10,10)']
