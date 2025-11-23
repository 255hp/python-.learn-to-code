# python-.learn-to-code
a python program that can be used for students data storage and grading


students = []

while True:
    print("\n------STUDENT MANAGER SYSTEM-----")
    print("1.add student")
    print("2. view student")
    print("3. update student score")
    print("4. remove student")
    print("5. Exit")
    
    choice = input("enter your choice(1-5): ")
    
    if choice == "1":
        name = input("enter the students name: ")
        age = int(input("enter students age: "))
        score = float(input("enter students scores: "))
        
        student = {
            "name": name,
            "age": age,
             "score": score
        }
        students.append(student)
        print("student succefully added! ")
    elif choice == "2":
    
      if len(students) == 0:
        print("no student is found")
      else :
        print("\n----- LIST OF STUDENTS-----")
        for i, student in enumerate(students, start=1 ):
            print(f"{i}. name: {student['name']}, age: {student['age']}, score: {student['score']}")
    elif choice == "3":
        if len(students) == 0:
            print("no student is available to update")
        else :
            print("\n----UPDATING STUDENT SCORE---")
            for i, student in enumerate(students, start=1):
             print(f"{i} {student['name']}, (curent_score: {student['score']})")
            
            index = int(input("enter student number to update: "))-1
            if 0 <= index < len(students):
                new_score = float(input("enter student new score: ")) 
                students[index] ['score'] = new_score  
                print("score update is successfull") 
            else:
                print("student number invalid")  
    elif choice == "4":
        if len(students) == 0:
            print("No student available to remove ")
        else:
            print("\n----REMOVING A STUDENT---")
            for i, student in enumerate(students, start=1):
                print(f"{i}. {student['name']}")
            index = int(input("enter the student number to remove: "))-1
            if 0 <= index < len(students):
                remove = students.pop(index)
                print(f"student '{remove['name']}' removed succefully ")
            else:
                print("invalid selection")
                
    elif choice == "5":
        print("Exiting the system....... Goodbye")  
        break
    else:
        print("invalid selection please choose between 1 and 5")          
    
        
            
            
            
            
    

    
        
         
