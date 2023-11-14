<img width="605" alt="1_wanna_b3_a_r0ck5tar_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/bc761535-99a2-4da2-a7df-05946e3f72b0">

This is a rockstar program and the key thing to understand is Poetic Number Literals in rockstar docs but it is not really necessary.

<img width="674" alt="1" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/822f398b-a11b-4338-9bde-295b2316eb8a">

Listen to is where the input is being asked and If makes the comparison. So we need to know the value of the_music and Music. I solved this by modifying the lyrics so that the if comparison is always true instead.

The original lyrics was:

```shell
Rocknroll is right              
Silence is wrong                
A guitar is a six-string        
Tommy's been down               
Music is a billboard-burning razzmatazz!
Listen to the music             
If the music is a guitar                  
Say "Keep on rocking!"                
Listen to the rhythm
If the rhythm without Music is nothing
Tommy is rockin guitar
Shout Tommy!                    
Music is amazing sensation 
Jamming is awesome presence
Scream Music!                   
Scream Jamming!                 
Tommy is playing rock           
Scream Tommy!       
They are dazzled audiences                  
Shout it!
Rock is electric heaven                     
Scream it!
Tommy is jukebox god            
Say it!                                     
Break it down
Shout "Bring on the rock!"
Else Whisper "That ain't it, Chief"                 
Break it down 
```

I changed the if lines like so to make them always true.

```shell
...
Listen to the music             
If the music is the music                 
Say "Keep on rocking!"                
Listen to the rhythm
If the rhythm is the rhythm
Tommy is rockin guitar
...
```
Running the program will ask for 2 inputs just enter any number. Convert the output from decimal to string to get the flag.
<img width="674" alt="2" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/645d913a-bddd-4f70-9c68-211c12c60fda">


```shell
picoCTF{BONJOVI}
```

