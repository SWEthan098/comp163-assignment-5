# comp163-assignment-5
Starting_num = int(input("Enter starting number: "))
#Step count is how man iterations it goes over
step_count = 0
Sequence = [Starting_num]
while Starting_num != 1:

#Need to use while loop because I have no idea when it ends 
    if Starting_num > 0:
        #Handles negatives 
        if Starting_num % 2 == 0:
           #Makes sure its a even number
           Starting_num = Starting_num // 2    
           #Does the calculation
        
        else:
            Starting_num = (Starting_num * 3) + 1
            
        Sequence.append(Starting_num)
        #Append adds the new Starting num after the calculations 
        step_count += 1
        #Compound operator adds 1 to the step count everytime the loop goes through
sequence_output = ""
for i in range(len(Sequence)):
    if i < len(Sequence) - 1:
        sequence_output += str(Sequence[i]) + "  "
    else:
        sequence_output += str(Sequence[i])
print(f"Sequence: {sequence_output}")
print(f"Steps: {step_count}")
