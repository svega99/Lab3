# Blueprint Management 1
In this exercise, a classes model will be built for the logical layer of an application that allows managing architectural plans of a prestigious design company.
## Part I


Configure the application to work under a dependency injection scheme, as shown in the previous diagram.

The above requires:

1.	Add the dependencies of Spring. Add the Spring settings. Configure the application - by means of annotations - so that the persistence scheme is injected when the BlueprintServices bean is created. Complete the getBluePrint() and getBlueprintsByAuthor() operations. Implement everything required from the lower layers (for now, the available persistence scheme InMemoryBlueprintPersistence) by adding the corresponding tests in InMemoryPersistenceTest.

	Se añaden las anotaciones.
	
	![Alt text](img/1.1.PNG)
	
	Se complementan los metodos  getBluePrint() y getBlueprintsByAuthor() en el service. 
	
	![Alt text](img/1.2.PNG)
	
	Se añade las anotaciones.
	
	![Alt text](img/1.3.PNG)
	
	Se implementan los metodos  getBluePrint() y getBlueprintsByAuthor()
	
	![Alt text](img/1.4.PNG)

2.	Make a program in which you create (through Spring) an instance of BlueprintServices, and rectify its functionality: register plans, consult plans, register specific plans, etc.


	![Alt text](img/2.1.PNG)
	
	![Alt text](img/2.2.PNG)
	
	![Alt text](img/2.3.PNG)
	

3.	You want the plan query operations to perform a filtering process, before returning the planes consulted. These filters are looking to reduce the size of the plans, removing redundant data or simply sub-sampling, before returning them. Adjust the application (adding the abstractions and implementations you consider) so that the BlueprintServices class is injected with one of two possible 'filters' (or possible future filters). The use of more than one at a time is not contemplated:

	![Alt text](img/3.1.PNG)
	
	![Alt text](img/3.2.PNG)

	1.	Redundancy filtering: deletes consecutive points from the plane that are repeated.
			
		![Alt text](img/3.3.PNG)
	

	2.	Subsampling filtering: suppresses 1 out of every 2 points in the plane, interspersed. 
	
	
		![Alt text](img/3.4.PNG)

4.	Add the corresponding tests to each of these filters, and test its operation in the test program, verifying that only by changing the position of the annotations - without changing anything else - the program returns the filtered planes in the way (A) or in the way (B).

		
	![Alt text](img/41.PNG)
	
	![Alt text](img/4.1.PNG)
	
	![Alt text](img/4.2.PNG)
	
	![Alt text](img/42.PNG)
	
	![Alt text](img/4.3.PNG)
	
	![Alt text](img/4.4.PNG)
	
