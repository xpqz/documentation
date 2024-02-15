# Penguin Class Example

The Penguin Class example illustrates the use of Interfaces to implement *multiple inheritance*.

[FishBehaviour Interface](FishBehaviour%20Interface.htm)

[BirdBehaviour Interface](BirdBehaviour%20Interface.htm)

[Penguin Class](Penguin%20Class.htm)

In this case, the `Penguin` Class derives from `Animal` but additionally supports the `BirdBehaviour` and `FishBehaviour` Interfaces, thereby inheriting members from both.
```apl
      Pingo←⎕NEW Penguin
      ⎕CLASS Pingo
  #.Penguin  #.FishBehaviour  #.BirdBehaviour    #.Animal
 
      (FishBehaviour ⎕CLASS Pingo).Swim
I can dive and swim like a fish
      (BirdBehaviour ⎕CLASS Pingo).Fly
Although I am a bird, I cannot fly
      (BirdBehaviour ⎕CLASS Pingo).Lay
I lay one egg every year          
      (BirdBehaviour ⎕CLASS Pingo).Sing
Croak, Croak!           
```
