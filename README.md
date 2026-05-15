# 2b IMPLEMENTATION OF SLIDING WINDOW PROTOCOL
## AIM
## ALGORITHM:
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
# Sliding Window Protocol Simulation
```
window_size = int(input("Enter window size: "))
total_frames = int(input("Enter number of frames: "))

sent = 0

while sent < total_frames:
    
    # Send frames in current window
    print("\nSending frames:")
    
    for i in range(sent, min(sent + window_size, total_frames)):
        print("Frame", i, "sent")
    
    # Receive acknowledgment
    print("Acknowledgment received for frames",
          sent, "to",
          min(sent + window_size - 1, total_frames - 1))
    
    # Move window
    sent += window_size

print("\nAll frames sent successfully")
```

## OUPUT
<img width="466" height="452" alt="image" src="https://github.com/user-attachments/assets/52d44f81-2106-4af7-b022-03b351e12397" />

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed
