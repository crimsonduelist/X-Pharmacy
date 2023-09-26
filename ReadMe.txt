/*This is so that the process of checking our project goes smoothly.
	
	**All the code is in said file(X-sql.txt) AND IN ORDER there is no code here, this is
	just a guide explaining the process.(Notes are also provided in X-sql.txt itself).
	The whole thing can be run at once or u can choose to copy paste step by step(That s what the notes are for)

---->BASICALLY RUN X-sql.txt THEN RUN X-plsql.txt THEN RUN PROGRAMM
	 LOGIN AS ADMIN.MAKE A SELLER.LOGIN AS SELLER.MAKE A PHARMACIST.LOGIN AS PHARMACIST

"STEP 1"		//STEPS 1-3 IS "FIRST PART" OF X-sql.txt

In sqldeveloper CREATE A USER "xaccess identified by pass" and grant him privileges


("xaccess" is the username "pass" is the password)
(EXACTLY AS IS IN QUOTES as this will be used in netbeans)
(making use of a user with sufficient privileges like system)


"STEP 2"		//"SECOND PART" OF X-sql.txt
In sqldeveloper CREATE A CONNECTION (the name doesnt matter) USING THE USER FROM "STEP 1"
(you can use the "+" sign from sqldeveloper)

"STEP 3"
OK. Now CONNECT with what u ve just created (you can double click on the connection from "STEP 2",
using the user name and password from "STEP 1")

"STEP 4"

CREATE TABLE statements + ALTER TABLE statements + CREATE SEQUENCE statements 
+ INSERT STATEMENT

(only 1 entry in the db as it stands. There are sample inserts and 
annonymous blocks("STEP 5" PROCEDURES X-plsql.txt) available IN "NOT_NEEDED.txt".
BUT I DO NOT RECOMMEND IT UNLESS YOU WANT TO ALSO CHECK STUFF MANUALLY OR ARE CURIOUS TO SEE HOW THEY
OPERATE.
I HAVE NOT HAD THE TIME TO CHECK THEM AGAIN AS THAT WAS NOT PART OF OUR SCHEDULE(adding said sample code)
THAT IS, THEY WORK BUT MIGHT CONFUSE OR LEAD TO MISTAKES)

"STEP 7"
RUN X-plsql.txt 
//This takes care of all the procedures(for example: inventory stock is 
added quantity in drugs)

"STEP 6"
The rest of the db entries can be now added directly using netbeans.
So unzip and open and run the project in netbeans. (libraries were included but just in case as mentioned
													in the .docx and .pdf along with version etc
													they re JDK 14 AND ojdbc8.jar)

"STEP 7"		// NAVIGATING / USING THE PROGRAM 
THE PROCCESS IS AS FOLLOWS:		
//IN ORDER
-> LOGIN AS ADMIN (WITH "ID" AND "PASS" FROM STEP 4 INSERT)
	->ADMIN CAN CREATE SELLER. 
	->ADMIN ADDS A DRUG("DRUGS" PAGE)  
//(pass in every new creation(seller or pharmacist) will be "0000".
//You can see the ID from the table provided right in the program)
	->ADMIN CAN NOW ADD IN INVENTORY/STOCK PRODUCTS("INVENTORY" PAGE) FROM SAID DRUG
-> LOGIN AS THE SELLER YOU JUST CREATED 
	->SELLER CAN CREATE A PHARMACIST
	->SELLER CAN NOW PLACE AN ORDER("ORDERS" PAGE)
	//For orders use the drug you created above (sellers and pharmacists can also see drug information
	in the "DRUGS" PAGE)
	->SELLER CAN ALTER HIS INFORMATION AND/OR PASSWORD
->LOGIN AS THE PHARMACIST YOU JUST CREATED
	->PHARMACIST CAN NOW PLACE AN ORDER("ORDERS" PAGE)