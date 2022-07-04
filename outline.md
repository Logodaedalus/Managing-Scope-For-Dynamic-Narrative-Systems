### Introduction

* Generative narratives enable new kinds of games you can’t make with static content, like
  * Games driven by deeply reactive character dialogue
  * System-driven games whose narrative reacts to game mechanics
  * Open world games whose narrative deeply responds to player actions / game state-space
  * and more!
* But writing content for dynamic narrative, compared to static forms, has design challenges that often makes shipping games with it difficult or infeasible
* If narrative designers and writers can figure out how to profile and design generative narratives while accounting for these challenges, then we can make these types of games more feasible
* I came up with a framework to help with that!
* This framework isn’t just theoretical for me
  * I created it by trying to generalize the lessons I learned from implementing and writing content for three systems in three different generative narrative “spaces”
    * Ice-Bound, which uses combinations of player actions to sculpt an evolving story
    * StoryAssembler, a hybrid system that combines an HTN planner with a forward state-space planner to generate choice-driven stories
    * Delve, a vignette generator that lets players change character memories by manipulating 3D objects
  * Each system had its own particular challenges, which I then tried to generalize out into the framework
* Hope it’s useful!

### Why Dynamic Narrative Systems, Anyway?

* Players have come to expect more from stories in games, especially when narrative is a central pillar
* Because of that, there's a push to create more dynamic and reactive narratives, requiring more sophisticated systems to tell them
* Creators, both in the AAA and indie space, turn to dynamic narrative systems to offer experiences that are 
  * more reactive to player actions
  * reactive to emergent game state (like simulations)
  * and thus more unique and compelling
* Dynamic narrative systems take work from the get-go...they’re not something that’s lightly slapped on at the end of a project
* Specifically, game designers employ them for very specific reasons, such as…
  * they want players to experience a sense of agency and control through making choices at key narrative points
    * Telltale games
  * they want players to experience a feeling of agency, but through affecting the gameplay system (which in turn affects the narrative)
    * King of Dragon Pass / Six Ages
  * the dynamism of the narrative system isn't necessarily the focus, but is an emergent requirement from the narrative needing to support reactive and dynamic gameplay
    * Skyrim’s “Radiant Story” system
  * Context-aware vignettes 
    * Hades or Horizon Zero Dawn

### What Are Their Production Problems?

* Those games sound great! Why isn’t everyone using these systems?
* It’s **not a tech challenge**. Most engineering required by dynamic narrative systems has been around for decades. Most tech in even the best cutting-edge dynamic narrative games _looks_ simple on paper.
* That’s because it’s a **design challenge**
* Also because writing content for these systems is way more work than most people think! 
* And if you don’t have a good design, it gets worse _very quickly_
* The more dynamic the narrative, the more expansive the interactivity, the more content required to surface that
  * Also, if you don’t account for the dynamism / interactivity when making your narrative system, creating and designing content can easily become more work than just writing static content to cover all your cases
* So making content isn’t just about quantity, but quality
  * sometimes even if dynamic content is created to broadly cover more interactions, and is reusable in different situations (so you need less of it overall), it incurs another problem: authoring complexity
  * authoring that kind of dynamic content can be so complex, it slows production down until the game's narrative could have been written faster using simpler, static methods, even though the volume of content needed would be much higher
* Systems where writing a huge amount of static content is faster than taking time to write smaller amounts of dynamic content, are being blocked by the “authoring wall”
* If you don’t overcome this, you’re in trouble!
