# Student-grade
students = []  
while True:
    name = input("Enter student name (or type 'exit' to finish): ")
    if name.lower() == 'exit':
        break
    try:
        marks = float(input("Enter marks (0–100): "))
        if marks >= 90:
            grade = 'A'
            comment = 'Excellent!'
        elif marks >= 75:
            grade = 'B'
            comment = 'Good Job!'
        elif marks >= 60:
            grade = 'C'
            comment = 'Needs Improvement'
        else:
            grade = 'F'
            comment = 'Failed'
        student_data = [name, marks, grade, comment]
        students.append(student_data)
        print(f"{name} scored Grade {grade} — {comment}\n")
    except ValueError:
        print("⚠️ Please enter valid numeric marks.\n")
print("\n📋 Final Results:")
for s in students:
    print(f"Name: {s[0]}, Marks: {s[1]}, Grade: {s[2]}, Comment: {s[3]}")
