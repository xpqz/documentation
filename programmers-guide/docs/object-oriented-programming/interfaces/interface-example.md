# Penguin Class Example

The Penguin Class example illustrates the use of Interfaces to implement *multiple inheritance*.

FishBehaviour Interface

BirdBehaviour Interface

Penguin Class

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

```apl
:Interface FishBehaviour
∇ R←Swim ⍝ Returns description of swimming capability
∇
:EndInterface ⍝ FishBehaviour
```

```apl
:Interface BirdBehaviour
∇ R←Fly ⍝ Returns description of flying capability
∇
∇ R←Lay ⍝ Returns description of egg-laying behaviour
∇
∇ R←Sing ⍝ Returns description of bird-song
∇
:EndInterface ⍝ BirdBehaviour
```

```apl
:Class Penguin: Animal,BirdBehaviour,FishBehaviour
    ∇ R←NoCanFly
      :Implements Method BirdBehaviour.Fly
      R←'Although I am a bird, I cannot fly'
    ∇
    ∇ R←LayOneEgg
      :Implements Method BirdBehaviour.Lay
      R←'I lay one egg every year'
    ∇
    ∇ R←Croak
      :Implements Method BirdBehaviour.Sing
      R←'Croak, Croak!'
    ∇
    ∇ R←Dive
      :Implements Method FishBehaviour.Swim
      R←'I can dive and swim like a fish'
    ∇
:EndClass ⍝ Penguin
```
