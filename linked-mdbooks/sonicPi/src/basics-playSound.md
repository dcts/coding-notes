# Playing Sounds

There are three ways to produce sound in SonicPi:
1. `play hz_to_midi 440` plays a sinewave with frequency 440 hz 
2. `use_synth :prophet` and `play 50` plays a note on a synth
3. `sample :mySample` plays a sample

### Examples
```ruby
# play 440 hz sinewave 
play hz_to_midi 440

# choose synth
use_synth :prophet
play 50

# use sample
sample :loop_amen_full
```

### Timing
```ruby
play 50     # play sound  
sleep 0.25  # sleep 0.25
play 60     # play sound 
sleep 0.25  # sleep 0.25
```

