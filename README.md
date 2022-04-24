# Multireplace For Sugarcube

This is a simple widget macro that replicates the function of multireplace from Choicescript. You can read more about multireplace [here](https://choicescriptdev.fandom.com/wiki/Multireplace) or try out the demo for this widget [here](https://merpati-katti.itch.io/sugarcube-multireplace-demo).

# General Usage
```<<mr $variablebeingtested "outcome 1" "outcome 2">>```

You can only use integers greater than 0 and booleans with this widget. Any other variable type will produce an error message.

# Usage: Positive Integers
Let's say you live in a fantasy town. Which of these would be your home?

    [[1. A royal castle.|NT 2][$home = 1]]
    [[2. The servant chambers of a lord's castle.|NT 2][$home = 2]]
    [[3. A spacious estate.|NT 2][$home = 3]]
    [[4. A farm near the riverbank.|NT 2][$home = 4]]
    [[5. An orphanage.|NT 2][$home = 5]]

_Each link changes the value of the $home variable, which will affect the output when using the multireplace widget. Try out the demo to see more._

```
So you hail from <<mr $home "a noble castle" "the chambers of maids" "a wealthy piece of land" "a ranch on the edges of town" "one of the many destitute orphanages">>, huh? Sounds like an interesting origin story.
```
   
# Usage: Booleans
_This example compares whether or not the user's pronouns are singular or plural. Try out the demo to see more._

```
<<upcase $they>> <<mr $singular "walks" "walk">> into the gardens, looking for a place to rest $their head. Having to be at the constant beck and call of others had really started to take a toll on $them. <<upcase $they>> <<mr $singular "is" "are">> only human, after all.
```
