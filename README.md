# Ex.No:4 To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Start App & Display First Screen
Launch the app.
Show the first screen (MainActivity) with:
EditText for user input (number)
Button labeled “Factorial”

Step 2: Get User Input
User enters a number in the EditText.
When the “Factorial” button is clicked:
Read the number from EditText.
Validate input (check if it’s not empty and is a positive integer).

Step 3: Use Explicit Intent to Open Second Screen
Create an Explicit Intent to start the second activity (ResultActivity).
Intent intent = new Intent(MainActivity.this, ResultActivity.class);
Pass the number to the second screen using Intent extras:
```
intent.putExtra("number", inputNumber);
```

Start the second activity:
startActivity(intent);


Step 4: Second Screen Receives Number
In ResultActivity’s onCreate() method:
Get the number from Intent:
```
int num = getIntent().getIntExtra("number", 0);
```

Step 5: Calculate Factorial

Initialize factorial = 1.
Loop from 1 to num:
```
for (int i = 1; i <= num; i++) {
    factorial *= i;
}
```
Or use BigInteger if large numbers.

Step 6: Display Result
Show the factorial in a TextView on the second screen.

Step 7: Optional Enhancements
Handle invalid inputs (empty or negative numbers) with a Toast message.
Use ScrollView if the factorial result is large.
Use BigInteger for very large numbers to prevent overflow.



## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
Developed by: THEJA SREE G
Registeration Number : 212224110056
*/
```

## OUTPUT

<img width="1723" height="950" alt="Screenshot 2025-09-16 105210" src="https://github.com/user-attachments/assets/13b75527-9de2-4500-847b-b2d5a0b2ad79" />

<img width="1919" height="1076" alt="Screenshot 2025-09-16 105225" src="https://github.com/user-attachments/assets/65b1bf13-7a8c-428d-ae09-487bbeeb85ec" />

<img width="1918" height="1078" alt="Untitled design (8)" src="https://github.com/user-attachments/assets/86a45e63-db9c-4441-be77-3d686db2315e" />

<img width="1918" height="1078" alt="Untitled design (11)" src="https://github.com/user-attachments/assets/ad04b50c-e0a1-44c1-838a-16627d7392d9" />



## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.


