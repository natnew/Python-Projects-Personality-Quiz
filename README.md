# Python Projects: Personality Quiz 🐍
This repo contains python code that generates a personality quiz and gives you a score based on your answers.<br>
Run the code.


Python
```python
print("Hello!")

# ask the candidate a question
activity = input("How do you spend your evening?\n(A Reading a book\n(B) Attending a party\n")

# print out which activity they chose
print(f"You chose {activity}.")

# if they chose reading a book
if activity == "A":
    print("Nice choice!")
elif activity == "B":
    print("Sounds fun!")
else:
    print("You must type A or B, let's just say you like to read.")
    activity = "A"

# ask the candidate a second question
job = input("What is your dream job?\n(A) Curator at the Smithstonian\n(B) Running a business\n")
if job == "A":
    print("Curator, nice choice!")
elif job == "B":
    print("Running a business? Sounds fun!")
else:
    print("You must type A or B, let's just say you want to be a curator at the Smithstonian")
    job = "A"

# Ask the candidate a third question
value = input( "What's more important?\n(A) Money\n(B) Love\n" )
if value == "A":
    print( "Money, nice choice!" )
elif value =="B":
    print( "Love? Sounds fun!" )
else:
    print("You must type A or B, let's just say money is more important to you.")
    value = "A"

# ask the candidate a fourth question
decade = input( "What's your favorite decade?\n(A) 1910s\n(B) 2010s\n" )
if decade == "A":
    print( "1910s, nice choice!" )
elif decade =="B":
    print( "2010s? Sounds fun!" )
else:
    print("You must type A or B, let's just say the 1910s is your favorite decade.")
    decade = "A"

# ask the candidate a fifth question
travel = input( "What's your favorite way to travel?\n(A) Driving\n(B) Flying\n" )
if travel == "A":
    print( "Driving, nice choice!" )
elif travel =="B":
    print( "Flying? Sounds fun!" )
else:
    print("You must type A or B, let's just say your favorite way to travel is by driving")
    travel = "A"

# print out their choices
print( f"You chose {activity}, then {job}, then {value}, then {decade}, then {travel}.")

# create some variables for scoring
sam_like = 0
cam_like = 0
kai_like = 0
indy_like = 0

# update scoring variables based on the activity choice
if activity == "A":
    sam_like = sam_like + 2
    indy_like = indy_like + 2
    kai_like = kai_like + 2
else:
    cam_like = cam_like + 1
    indy_like = indy_like + 1

# update scoring variables based on the job choice
if job == "A":
    sam_like = sam_like + 2
    indy_like = indy_like + 2
    cam_like = cam_like - 1
else:
    sam_like = sam_like - 1
    kai_like = kai_like + 2
    indy_like = indy_like + 1

# update scoring variables based on the value choice
if value == "A":
    sam_like = sam_like - 1
    kai_like = kai_like + 1
else:
    sam_like = sam_like + 2
    cam_like = cam_like + 2
    indy_like = indy_like + 1

# update scoring variables based on the decade choice
if decade == "A":
    cam_like = cam_like + 2
    sam_like = sam_like + 2
else:
    kai_like = kai_like + 1
    indy_like = indy_like + 2

# update scoring variables based on the travel choice
if travel == "A":
    sam_like = sam_like - 2
    kai_like = kai_like + 1
    indy_like = indy_like - 1
else:
    sam_like = sam_like + 1
    cam_like = cam_like + 1
    kai_like = kai_like - 1

# print the results depending on the score
if sam_like >= 3:
    print( "You're most like Sharp-Eyed Sam!" )
elif cam_like >= 3:
    print( "You're most like Curious Cam!" )
elif kai_like >= 3:
    print( "You're most like Keen Kai!" )
else:
    print( "You're most like Inquisitive Indy!" )
```

Output
```python
Hello, Contosoville!
How do you spend your evening?
(A Reading a book
(B) Attending a party
```
