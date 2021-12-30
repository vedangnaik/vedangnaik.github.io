---
layout: post
title: "On Techniques for Efficient 100% Steam Achievements in Desperados III"
---

<head>
    <style>
        .normal-difficulty {
            color: #f0b000;
        }
        .hard-difficulty {
            color: red;
        }
        .navigation-link {
            text-align: right;
            font-size: 12px;
        }
    </style>
</head>

I've been replaying [Desperados III](https://store.steampowered.com/app/610370/Desperados_III/) on PC recently. As I was going through the first few missions, I thought *Gee, it sure would be fun to do all these extra badges and maybe even 100% this game!* However, the badges for each mission do not show up until after the first completion, which leads to a ton of wasted time. One also ends up missing a lot of the secret achievements in each mission. Thus, I decided to create this 'roadmap' of sorts to allow one to 100% this game as efficiently as possible. I hope you find it useful!

<h3 style="color: red"> CAUTION! This post contains a lot of spoilers for the main game. </h3>
<br>
<br>




## Introduction

With that in mind, let's begin. First, some terminology:
* A 'map' is the landscape upon which your characters and enemies move around. Examples include *Devil's Canyon, Casa DeVitt*, etc. These names can be seen when hovering over the mission selectors in the 'Mission Select' menu. These have no specific formatting.
* A 'mission' is a set of objectives which you characters achieve on a map. Examples include *On the Hunt, Untitled Voodoo Mission*, etc. There are 16 missions in the main story, and 14 missions in the *Baron's Challenges*. These have no specific formatting.
* ***Steam achievements*** (or just ***achievements***) are the main focus on this article.
* A <u>badge</u> is a specific challenge associated with a story mission.
* Hyperlinked [words like these](#) will link to external resources like YouTube videos or other guides. Some information is best conveyed through these means.
* Character `skills` are highlighted like this. Examples include Cooper's `Fake Coin`, Isabelle's cat `Stella`, etc. These are not the full names as they appear in-game, but are clear enough regardless.

As of the writing of this post, the base game on Steam has 36 achievements. Some of these can be contributed to from any mission (e.g. ***They Wear Red Bandanas: Kill 75 Long Coats***) while others can only be done on certain missions (e.g. ***Lost and Found: Return the money to the bank***). This guide will go through the main story on a playthrough-by-playthrough basis mainly focussing on the latter, with an emphasis on 
* ***Sheriff's Badge: Earn 90 badges***: 14 out of the 16 main story missions have eight badges each. This gives us a total of 112 badges, out of which we must earn 90. Not all of the badges are equally easy to earn however, so I have chosen what are, in my opinion, the easiest ones to get for each mission. Note that all of the fourteen missions have <u>Complete the mission on Hard difficulty.</u> and <u>Speedrun: Complete the mission in under xx:xx minutes</u>. I've elected to always do the former, and only include the latter if there is a suitably easy strategy.
* ***Seasoned Bounty Hunter: Kill 15 of the hidden Mimimi devs*** and ***Veteran Bounty Hunter: Kill 31 hidden Mimimi devs***: The 'hidden Mimimi devs' are named NPCs which are found in out-of-the-way spots on most maps. [This guide](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement) shows all of their locations. It suffices to just kill them and wait a few moments; you don't have to finish the mission to have the kill count.

Each playthrough section will be coloured <span class="normal-difficulty">like so</span> if the difficulty is 'Normal' and <span class="hard-difficulty">like so</span> if the difficulty is 'Hard'. There will also be farming tips for some of the mission-agnostic achievements, if applicable. For these farming techniques, it suffices to create a quicksave just a second before the event, then reloading this over and over again until the desired number has been reached. For example, if farming for ***Doubletime: Kill 200 guards using Cooper's double shot***, use Showdown mode to make Cooper target two guards, then quicksave, then execute the action. After that, reload the quicksave and execute it again over and over. Even though you're killing the same guards again and again, it still counts as separate kills for the achievement.

I've also included some general tips to aid you on your playthroughs.

#### Navigation
<!-- no toc -->
- [Introduction](#introduction)
- [General Tips](#general-tips)
- [Main Story Missions](#main-story-missions)
  1.  [On The Hunt](#on-the-hunt)
  2.  [Byers Pass](#byers-pass)
  3.  [Troublemakers in Flagstone](#troublemakers-in-flagstone)
  4.  [Until Death Do Us Part](#until-death-do-us-part)
  5.  [O'Hara Ranch](#ohara-ranch)
  6.  [The Bridge at Eagle Falls](#the-bridge-at-eagle-falls)
  7.  [One Good Shot](#one-good-shot)
  8.  [One Hell of a Night](#one-hell-of-a-night)
  9.  [Louisiana Voodoo](#louisiana-voodoo)
  10. [Back Alley Jazz](#back-alley-jazz)
  11. [Burn the Queen](#burn-the-queen)
  12. [Dirt and Blood](#dirt-and-blood)
  13. [A Cart Full Of Gunpowder](#a-cart-full-of-gunpowder)
  14. [The Wages of Pain](#the-wages-of-pain)
  15. [A Captain Of Industry](#a-captain-of-industry)
  16. [The Old And The New](#the-old-and-the-new)
- [Baron's Challenges](#barons-challenges)
- [Conclusion](#conclusion)

<br>



## General Tips
In no particular order, here are some tips, mechanics, and notes that I've either noticed myself or learnt from speedruns and other sources.

* Possibly the most easily abusable mechanic in the game is that an *unconscious, tied-up guard* will lure *any guard* (even Ponchos and Long Coats) and furthermore, the lured guard(s) will not raise the alarm until *after* they've untied their friend. In some levels, this allows you to easily break open formations of three or four guards watching each other. Note, however, that once they've been lured, additional lures like Hector's `Whistle` and McCoy's `Bag` won't work.
* Cooper can easily deal with pair of guards by throwing his `Knife` at one and knocking out the other.
* Hector can `Whistle` to the same enemy twice. The second time, they'll come running, so be prepared to take them out quickly.
* In general, even if guards see you, you have a window of maybe half a second to kill them before they actually raise the alarm.
* Any time a character picks up a guard that another character has killed, any animation the body is in will get cancelled. For example, if Doc uses his `Buntline` on someone, the guard takes a very long time to fall down; this usually ends up being seen by somebody. Instead, you can have (say) Kate stand right next to the guard, then immediately pick them up the moment Doc shoots them. This will cancel the long fall-down animation and prevent anyone from seeing it.
* Isabelle's `Connect` is a very flexible tool that can be used in a variety of situations. Here are a few:
  * Long Coats connected to normal guards will get distracted by `Stella`.
  * Killing a guard connected to a Long Coat will cause the Long Coat to go into the stagger state.
  * Connecting Isabelle herself to another guard and then using `Mind Control` on a second guard will *kill* the connected guard (for some reason).
  * Killing guards by connecting them to someone killed via the environment does not raise an alert, no matter how far they are.
* All characters can drop bodies off of heights, and Hector can throw them. A body thrown onto a guard will knock them out; even Long Coats will get knocked out (they can then be killed normally). Specifically, Hector can throw bodies onto *your own characters* and *carry and throw them* as well! This is used in some speedruns to throw certain characters over short obstacles that they'd otherwise have to walk around.
* Hector, Isabelle, and `Mind Control` have a very nice synergy. After Isabelle `Mind Control`s a guard, she cannot move. This thus fixes the radius of the control. However, Hector can *knock her out* and then *carry her* to some other location, and the control's radius *will change* as well!
* Guards following Kate under her `Lure` will climb up/down ladders but will not continue following her through buildings or doors.
* Isabelle moves significantly faster than all the other characters.

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>




## Main Story Missions

### On The Hunt
This mission has no badges or Mimimi devs, but has a few secret achievements.

<h4 class="normal-difficulty">Playthrough #1</h4>

* Achieve ***[Lindberg and Hutch: Decide the outcome of a duel](https://www.youtube.com/watch?v=esaBl_teFSI)***.
* Achieve ***[Sorry, Dad!: Knock out your father](https://www.youtube.com/watch?v=jWd_AASN5QE)***.

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>




### Byers Pass
This is probably the easiest mission to complete in Desperado difficulty, so the last playthrough will focus on that. At the end of these playthroughs, you should have **7/90** badges.

<h4 class="hard-difficulty">Playthrough #1</h4>

* Achieve ***[The Picnic: Enjoy some cupcakes during a picnic](https://www.youtube.com/watch?v=esaBl_teFSI)***.
* Shoot the first golden chicken for ***[Chicken Dinner: Kill all 3 golden chickens](https://guides.gamepressure.com/desperados-iii/guide.asp?ID=58096)***.
* Earn <u>Save all groups of civilians</u>. This is straightforward, except for the last civilian being interrogated by Big Ann: you must move quickly to kill her before she kills him.
* Achieve ***[Kaboom!: Kill 5 guards at once with dynamite](https://www.youtube.com/watch?v=Ox_FC5DDJ10)*** and earn <u>Kill 3 bandits at the same time</u> at once.
* Earn <u>Kill 10 bandits using dynamite</u>. Just make sure to leave enough guards alive for this by the end.
* Earn <u>Distract 3 bandits at the same time using Cooper's coin</u> by tossing a coin at the three bandits standing under the big rock.
* Earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.
* Kill the [two Mimimi developer NPCs](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement).
* [Optional] Farm for ***Doubletime: Kill 200 guards using Cooper's double shot*** and ***Damn Good Marksman: Snipe 50 guards with McCoy***.

<h4 class="normal-difficulty">Playthrough #2</h4>

* Earn <u>Don't save during the mission</u>. You can explicitly set the number of saves to 'None' in the difficulty options if you reflexively save like I do 😂. Go slowly and ensure that you can safely proceed. It's not the end of the run if you trigger an alert: just wait it out.
* Earn <u>Don't use firearms</u>. This is fairly straightforward. Rely on McCoy's `Bag` and Cooper's `Knife`. Note that for pairs, Cooper can use `Knife` on one guard and immediately knock out the other.

<h4 style="color:purple">Playthrough #3</h4>
* Achieve ***Hardcore: Finish a mission on "Desperado" difficulty*** by completing this mission in 'Desperado' difficulty.

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>




### Troublemakers in Flagstone
At the end of these playthroughs, you should have **14/90** badges.

<h4 class="hard-difficulty">Playthrough #1</h4>

* Earn <u>Make the deaths of 4 targets look like accidents</u>. To do so, poison Wild Marge, provoke the bull to kill Jarvis, drop the church bell onto The Duke, and drop the incomplete building wall onto McBane.
* Earn <u>Bury Josh</u>. In the church area, there's a NPC named "Josh". After killing him, throw him into the open grave in the church courtyard to earn this.
* Earn <u>Listen in on 10 private conversations</u>. The various conversations are marked by comic-book speech bubbles.
* Earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.
* Kill the [two Mimimi developer NPCs](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement).
* [Optional] Farm for ***They Wear Red Bandanas: Kill 75 Long Coats***.

<h4 class="normal-difficulty">Playthrough #2</h4>

* Earn <u>Kill 3 mission targets at the same time</u>. This is a little finnicky, but not overly so. You must poison Wild Marge, and then, the moment her mission indicator becomes green, kill two others. I killed McBane and The Duke with Cooper's dual `Revolvers` from the top of the cliff near the church, but there are alternate methods. Note that this will set of an alert, but you can just wait for it to clear up and then re-enter the civil zone.
* Earn <u>Don't kill or knock out anyone in the train track area</u>. This doesn't apply to McBane, in case you were wondering.
* Earn <u>Don't touch any bushes or haystacks</u>. This isn't as hard as it sounds. Approach Wild Marge's building from the right, and Jarvis' area from the left.

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>




### Until Death Do Us Part
The badges for this level *cannot* be done simultaneously, so we are forced to do multiple playthroughs. At the end of these playthroughs, you should have **20/90** badges.

<h4 class="hard-difficulty">Playthrough #1</h4>

Get the disguise for this playthrough if you wish.
* Earn <u>Take a photo of the dead groom</u>. **Important!** This is an easy badge to *lock* yourself out of: you must pick up the Mayor's body and throw it down *before* you make Cooper and Kate jump off the balcony. Once they're down, there's no way to go back up there. Afterwards, it's fairly straightforward to carry his body to the camera and take the photo.
* Earn <u>With Cooper, enter the building through the main balcony door</u>. **Important!** This is another easy badge to lock yourself out of: in the Kate-only part, you must make sure to *unlock the main balcony door* before the cutscene, otherwise Cooper can't enter.
* Earn <u>Don't use the Gatling Gun</u>.
* Earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.
* Kill the [two Mimimi developer NPCs](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement).

<h4 class="normal-difficulty">Playthrough #2</h4>

* Earn <u>Don't use a disguise</u>. This isn't as hard as it sounds; you just have to be careful and use Kate's perfume cleverly.
* Earn <u>Kill 15 guards with the Gatling Gun</u>. Since you don't have the disguise, you have my green light to use the gun 😎.

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>



### O'Hara Ranch
This mission has a pretty straightforward [speedrun strategy](https://www.youtube.com/watch?v=TYcpPkJNkAk), executed here by speedrunner *Optibum*. Thus, the speedrun badge will be included. At the end of these playthroughs, you should have **28/90** badges.

<h4 class="hard-difficulty">Playthrough #1</h4>
This is the non-speedrun playthrough. In any case, try to follow the same route to get a feel for it.

* Earn <u>Kill all Long Coats</u>. **Important!** While this badge is self-explanatory, it must be done *before* you get McCoy and Hector to the rooftop for the second part of the level.
* Earn <u>Finish the mission without using a torch</u>. Note that even picking up a torch counts as 'using' it. You can shoot enemies carrying lanterns over oil puddles to light them instead.
* Earn <u>Win the bet with Hector</u>. If you're paranoid, you can switch McCoy to non-lethal mode.
* Earn <u>Burn 15 guards in oil puddles</u>. This can be 'manually' done by knocking out 15 guards and using Hector and McCoy to place them on an oil puddle, then lighting it on fire. Make sure to do one set of five to achieve ***Inferno: In the first part of the mission, burn 5 guards at once with oil traps***.
* Achieve ***[M-M-M-M-MONSTER KILL: Kill 6 guards at once using only a single skill](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement)*** by placing some knocked-out guards in a pile and then using Hector's `Sawed-off` on them.
* Earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.
* Kill the [two Mimimi developer NPCs](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement).
* [Optional] Farm for ***Good Girl: Kill 75 guards with Bianca***, ***Another One Bites the Dust: Kill 500 guards*** and ***Someone Call the Undertaker: Kill 1,000 guards***.

<h4 class="normal-difficulty">Playthrough #2</h4>
This is the speedrun playthrough.

* Earn <u>Win the bet with McCoy</u>. The speedrun route relies heavily on McCoy, so you should earn this naturally.
* Earn <u>Speedrun: complete the mission in under 17:00 minutes</u>. Make sure you have adequately memorized what each character is supposed to do. Play smoothly and calmly; 17 minutes is more than enough time for this route. Optibum makes some risky plays to avoid waiting for guard rotations, but you can afford to wait for them.
* * Earn <u>Don't save during the mission</u>. This should be straightforward if you've sufficiently practiced the route.

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>




### The Bridge at Eagle Falls
At the end of these playthroughs, you should have **35/90** badges.

<h4 class="hard-difficulty">Playthrough #1</h4>

* Earn <u>Get the dynamite from the quarry</u>. I feel the quarry is easier to deal with on Hard difficulty than the shooting range.
* Earn <u>Kill 3 guards at the same time in a quarry explosion</u>. This is easy to do on the way to the previous badge. Note that the explosion is instantaneous, so you can run and detonate it if needed.
* Earn <u>Kill 5 guards when destroying the bridge</u>. To do this, place 5 unconscious guards on the section of the bridge just above where the dynamite goes. During the cutscene, this part will fall away and you'll receive the badge.
* Achieve ***Goodbye Colorado: Blow up a bridge*** and earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.
* Kill the [two Mimimi developer NPCs](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement).

<h4 class="normal-difficulty">Playthrough #2</h4>

* Earn <u>Get the dynamite from the shooting range</u>.
* Earn <u>Don't use firearms</u>. This places a rather major restriction on this level, but it is still quite straightforward. I feel the shooting range is easier to handle without guns since you have multiple approaches. McCoy's `Swamp Gas` can be used to take out the Long Coat. It's also en route to the next badge.
* Earn <u>Kill 3 guards with rolling logs</u>. The logs are near the sawmill adjacent to the shooting range. With her disguise, Kate can easily walk there and release the logs.
* [Optional] Farm for ***Follow Me Darling: Make guards follow Kate for 1,000 meters total*** and ***Watch Out Below!: Kill 50 guards using the environment***.

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>




### One Good Shot
This mission has no badges or secret achievements, but has a single Mimimi dev.

<h4 class="normal-difficulty">Playthrough #1</h4>

* Kill the [Mimimi developer NPC](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement).

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>




### One Hell of a Night
The *unconscious-and-tied-up guard lure mechanic* along with the footsteps-in-the-mud mechanic and Hector's ability to carry, run, and throw bodies makes him *extremely overpowered* in this level. So much so, in fact, that's its possible to get all 7 badges in a single playthrough! At the end of this playthrough, you should have **42/90** badges.

<h4 class="hard-difficulty">Playthrough #1</h4>

* Achieve ***Lost and Found: Return the money to the bank*** and earn <u>Return the money to the bank</u>. <b>Important!</b> This is an easy badge to lock yourself out of. At the very start of the mission, use Hector to knock out the woman outside the hut. She'll drop the money, which Hector can pick up. Drop this onto the floor of the bank in the same room where McCoy is being held to get the achievement and badge. If you wait until after you rescue McCoy, she will disappear and they will no longer be obtainable.
* Earn <u>Free Doc before waking up the others</u>. This is quite easy since almost every guard in the vicinity can be lured away.
* Earn <u>Don't use a disguise</u>. In fact, Kate doesn't even need to do anything at all.
* Earn <u>Kill 6 guards</u>. You can throw guards into the water to kill them. You can also kill up to 3 guards using the cannon in the middle of the level.
* Earn <u>Don't use the bank's backdoor</u>. The 'backdoor' refers to the entrance from the construction area.
* Achieve ***Yakety Sax: Make someone follow your footprints for 25 meters.*** and earn <u>Make a guard follow your footprints for 50 meters</u>. This requires a bit of timing, but can be done immediately at the very beginning of the mission. Lure the guard near the water tower. Use the incline the hut is on to break his line of sight, and keep circling around it until you receive the badge.
* Earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.
* Achieve ***[Need a Dentist?: Find a patient for the dentist](https://www.youtube.com/watch?v=9-tsCaqHAOM)***. This is best done at the end after you've cleared most of the map.
* Kill the [three Mimimi developer NPCs](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement).

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>




### Louisiana Voodoo
After these playthroughs you should have **47/90** badges.

<h4 class="hard-difficulty">Playthrough #1</h4>

* Earn <u>Free Kate or Hector first</u>. I believe you can immediately swim across to Kate's cell from the beginning of the level.
* Earn <u>Kill 3 guards with an environment kill</u>. At the very beginning, the `Mind Control`ed guard can be used to kill the two guards under the pile of boxes. After that, there's a single guard under a big rock near Cooper's boat.
* Achieve ***Like Clockwork: Execute a plan with all five characters*** and earn <u>Kill 5 guards at the same time</u>. Note that for the achievement, if suffices to just make a character walk somewhere in Showdown Mode if you don't have anything specific for them to do.
* Earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.
* Shoot the second golden chicken for ***[Chicken Dinner: Kill all 3 golden chickens](https://guides.gamepressure.com/desperados-iii/guide.asp?ID=58096)***.
* [Optional] At the very beginning, you can farm for ***Puppet Master: Mind control 25 guards with Isabelle***. Once you have all five characters, you can batch farm for ***Out of Sight, Out of Mind: Hide 250 bodies*** and ***Maneater Shrub: Hide 750 bodies***.

<h4 class="normal-difficulty">Playthrough #2</h4>

* Earn <u>Don't touch water</u>. This playthrough is mostly for this badge since it's so restrictive. Note that this doesn't just mean you can't swim; a single <i>touch</i> of water invalidates this badge. Thus, keep checking the status regularly to make sure that no character accidentally walked through a puddle or something somewhere.
* Achieve ***Seasoned Bounty Hunter: Kill 15 of the hidden Mimimi devs*** by killing the [two Mimimi developer NPCs](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement). McCoy take them out easily.
* [Optional] If you wish you can try the alternative badge <u>Don't use Isabelle's connect ability</u>.

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>





### Back Alley Jazz
After these playthroughs you should have **53/90** badges.

<h4 class="hard-difficulty">Playthrough #1</h4>

* Earn <u>Don't kill anyone</u>. This is a little tedious, but not overly difficult. Make sure to switch all characters to their non-lethal mode by default to avoid mistaken kills.
* Earn <u>Don't kill any suspects</u>. You can't kill *anyone*, the suspects count.
* Earn <u>Get information on aliases and locations for all suspects</u>. This is best done after acquiring Kate's disguise, which is very easy to do.
* Earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.

<h4 class="normal-difficulty">Playthrough #2</h4>

* Achieve ***[Exterminator: Kill 10 small animals in one mission](https://knoef.info/trophy-guides/ps4-guides/desperados-3-trophy-guide/)***. **Important!** This is an easy achievement to lock yourself out of. The animals are scattered throughout both 'phases' of the mission, and if you don't kill them before proceeding to phase 2, you won't get the achievement. I also found the animals bugged; a little bit of noise was needed to make them move around. Make sure to quicksave and reload often.
* Earn <u>Kill all suspects</u>.
* Earn <u>Kill 3 guards using dogs</u>. You must `Mind Control` the dog and force it to bite a guard. You will need at least 2 darts for this. Make sure to use Isabelle to connect two guards together to get more bang for you bark 😉.
* Kill the [three Mimimi developer NPCs](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement), since you're now allowed to kill.

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>




### Burn the Queen
After these playthroughs you should have **59/90** badges.

<h4 class="hard-difficulty">Playthrough #1</h4>

* Earn <u>Kill everyone except for civilians</u>. Make sure to not knock out, tie up, and throw guards into bushes; if they disappear, this badge will become unobtainable. Note that this badge also appears to include the reinforcements that arrive after you set the boat on fire; use Hector's `Sawed-off` to deal with them the moment they exit the guard house.
* Earn <u>Open all cages</u>.
* Earn <u>Hide all bodies in bushes, wells, houses, etc</u>.
* Achieve ***Wait, Did You Say Marshal?: Find Wayne*** and earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.
* Kill the [two Mimimi developer NPCs](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement).

<h4 class="normal-difficulty">Playthrough #2</h4>

* Earn <u>No knockouts or melee kills except for Isabelle</u>. This isn't as difficult as it sounds; you're still allowed to use Cooper's `Knife` and dual `Revolvers`, Hector's `Bianca`, and McCoy's `Buntline`.
* In fact, also earn <u>Don't use McCoy's snipe</u> by forgoing the `Buntline` as well.

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>




### Dirt and Blood
This is not a level I enjoyed playing, so I apologize in advance if the playthroughs below aren't as efficient as they could be. Regardless, after these playthroughs you should have **65/90** badges.

<h4 class="hard-difficulty">Playthrough #1</h4>

* Earn <u>Kill 3 guards using the steamer wheel</u>. I arbitrarily decided to do this first, but it may be easier with the disguise.
* Earn <u>Choose the path on the left</u>: The steamer wheel from the previous badge is is in the pier on the left side of the map. Note that the 'path' isn't locked until any character reaches the last stretch of street before the meeting point.
* Earn <u>Don't use a disguise</u>. The left side route is quite tedious without the disguise, but it's doable. I think the right side may be easier without the disguise, but I didn't play that to confirm.
* Achieve ***Goodbye Louisiana: Meet Frank on a boat*** and earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.

<h4 class="normal-difficulty">Playthrough #2</h4>

* Earn <u>Choose the path on the right</u>.
* Earn <u>Kill all Long Coats</u>. Make sure to use the disguise to simplify this.
* Kill the [two Mimimi developer NPCs](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement).

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>




### A Cart Full Of Gunpowder
After these playthroughs you should have **71/90** badges.

<h4 class="hard-difficulty">Playthrough #1</h4>

* Earn <u>Don't use Isabelle's connect ability</u>. This places a fairly major restriction on the level, but even in Hard difficulty it's still pretty straightforward.
* Earn <u>Traverse the mine on the left side</u>. I found the left side easier than the right due to the larger number of environmental kills. Since you don't have `Connect`, I recommend this path.
* Earn <u>Kill 20 opponents with dynamite</u>. Again, since you don't have `Connect`, go ahead and just blow everybody up 😎. Be careful, however - your characters have lesser health in hard difficulty, so they can't get shot too often.
* Earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.
* Kill the [**first of two** Mimimi developer NPCs]("https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement").
* [Optional] If you wish, you can try to earn <u>Pick up only McCoy's gear</u>; you will automatically earn the first badge since `Connect` is part of Isabelle's 'gear'. This may be very tedious, however.

<h4 class="normal-difficulty">Playthrough #2</h4>

* Earn <u>Don't pick up the dynamite</u>. Since you have `Connect` now, you can afford to be more discreet.
* Earn <u>Traverse the mine on the right side</u>.
* Kill the [**second of two** Mimimi developer NPCs]("https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement") on the way to the previous badge.

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>





### The Wages of Pain
This is not a level I enjoyed playing, so I apologize in advance if the playthroughs below aren't as efficient as they could be. Regardless, after these playthroughs you should have **77/90** badges.

<h4 class="hard-difficulty">Playthrough #1</h4>

* Achieve ***[Power Nap: Interrupt an important healing procedure](https://www.youtube.com/watch?v=o8mm3fDr1bQ)*** at the very beginning of the mission.
* Earn <u>Finish the mission without crossing the train tracks</u>. This places a fairly major restriction on the level but it it still manageable.
* Earn <u>Kill 5 guards with the train</u>. You can do this by knocking out guards and dropping them onto the tracks. Alternately, for a more 'entertaining' approach, you can use Hector's `Whistle` on guards on the other side at the exact moment to have them run over by the train.
* Earn <u>Use the wagon to block the train tracks</u>. Make a **manual save** before you do this; on the next playthrough, you can reload this to get the stuff on the other sides of the tracks quickly.
* Earn <u>Finish the mission without dropping Isabelle</u>. This is easier than it sounds. You can't use Cooper, but since he's alone on the other side of the map there's not much he can do anyway. Since Kate and Hector are already at the front of the train, you'll have a much easier time taking out guards with them.
* Earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.
* Kill the [**first of two** Mimimi developer NPCs]("https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement").

<h4 class="hard-difficulty">Playthrough #2</h4>
Reload your **manual save** from the previous playthrough.

* Earn <u>Use the cattle to block the train tracks</u>. Once you earn this, you can quit the mission; the badge is counted instantly.
* Achieve ***[Gunslinger's Creed: Jump from a tower into a cart of hay](https://www.youtube.com/watch?v=130AHX6nNOY)*** on the way to the previous badge.
* Kill the [**second of two** Mimimi developer NPCs]("https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement").

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>




### A Captain Of Industry
This mission has a very easy [speedrun strategy](https://www.youtube.com/watch?v=UovLY9SbneY), executed here by *Optibum* again. Thus, the speedrun badge will be included. In fact, by making small tweaks here and there to this route, you can very easily earn all eight badges inside 30 minutes. After these playthroughs you should have **85/90** badges.

<h4 class="normal-difficulty">Playthrough #1</h4>
This is the speedrun playthough; the time limit is generous enough that it can be done first time, along with with a small change to earn an extra badge.

* Earn <u>Don't use both distractions</u>; this is automatically achieved by this route.
* Earn <u>Don't let anyone see you</u>. The 22 minutes for the speedrun badge is more than enough to execute this route. Thus, take your time and avoid being spotted.
* Earn <u>Use mind control on Devitt's character</u>; this is automatically achieved by this route. Note that some online guides say that this badge cannot be earned unless one of the distractions has been used and DeVitt is alone with his men - this is **false** (at least as of writing this post); you can get it at any point.
* Earn <u>Kill 2 guards with a statue</u>. Immediately after relinquishing `Mind Control` on DeVitt and securing him, use Hector to drop the statue in the courtyard onto the guard and the Long Coat. If you miss a rotation, don't worry; you have enough time to do this and still get the speedrun badge.
* Earn <u>Speedrun: Complete the mission in under 22:00 minutes</u>. Make sure you have memorized everything that each character has to do. Play smoothly and calmly; you have enough time. The last section is a little finnicky; I found that connecting a few guards and then using `Stella` on them helps.
* Achieve ***Package Delivered: Take care of DeVitt*** by completing this playthrough.

<h4 class="hard-difficulty">Playthrough #2</h4>
This follows the same route as earlier, but with more substantial changes. If you didn't get the speedrun badge, I recommend trying again in normal mode and doing this playthrough without time pressure. Make sure to make a **manual save** before finishing this playthrough; continue reading for more details.

* Earn <u>Don't touch any bushes or haystacks</u>. Follow the same route as earlier, but make sure to not touch any bushes or haystacks. This makes Isabelle and Hector's section slightly more complicated.
* Earn <u>Don't use any of Kate's or Cooper's skills</u>. This is easier than it looks, since neither of them actually do much on this route. Substitute Cooper's kills with Isabelle and `Connect`, and Kate's `Perfume` with `Stella`. Note that Cooper's tying up of a unconscious person counts as a 'skill'. Both Kate and him can still carry bodies, however. In the last section, use Hector and Isabelle to kill all guards and knock out all civilians.
* Earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.
* Once you've earned the three badges above, reload your **manual save** and kill DeVitt and achieve ***Vendetta: Kill DeVitt***.
* Reload your manual save once again and backtrack with Cooper to kill the [two Mimimi developer NPCs]("https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement")

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>





### The Old And The New
I found this mission very long and tedious, and I think many other people felt the same. Thus, I decided to do a single playthrough and earn just 5 badges here. It is challenging enough with the added constraints of the five badges, so we'll be forgoing the Hard difficulty badge as well. After this playthrough you should have **90/90** badges.

<h4 class="normal-difficulty">Playthrough #1</h4>

* Earn <u>Don't switch sides with any character</u>. This places a major restriction on this playthrough, but is still fairly bearable. Note that it is unclear at what point a character is considered to have 'crossed-over' when on the first bridge at least; I personally kept them completely off it and ignored the central section.
* Earn <u>Reach the chapel via the right entrance</u>. This badge is earned the moment Isabelle or McCoy *cross the rope bridge* leading to the chapel area. Make sure to make a **manual save** before doing this; after you cross the bridge and earn the badge, load this save and then do the badge below.
* Earn <u>Reach the chapel via the left entrance</u>. This badge is earned the moment Cooper, Kate, or Hector cross the *thin, rocky path* leading to the chapel area.
* Earn <u>Kill 6 guards with falling rocks</u>. This can be done very early by Isabelle and McCoy on the right side path. To do so, knock out the eight guards in the vicinity and place them under the boulder before pushing it over.
* Earn <u>Don't use a disguise</u>. This is easier than it sounds. In any case, it's unclear if one can obtain the disguise without 'crossing over'.
* Achieve ***Veteran Bounty Hunter: Kill 31 hidden Mimimi devs*** by killing the [two Mimimi developer NPCs]("https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement").
* Achieve ***[Chicken Dinner: Kill all 3 golden chickens](https://guides.gamepressure.com/desperados-iii/guide.asp?ID=58096)*** by shooting the final golden chicken.
* Achieve ***Five Good Shots: Defeat Frank*** and ***Sheriff's Badge: Earn 90 badges*** by completing this playthrough.

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>




## Baron's Challenges

At this point, the only achievement you should have left is ***Most Entertaining: Complete 5 of the Baron's Challenges***. Since you've finished the main story, you will have all 14 challenges unlocked, out of which you must do five. Note that you can complete them on normal difficulty if you wish; in fact, even beginner difficulty may suffice, though I haven't tested this. Here are my recommendations - I chose them since they all have fairly straightforward speedruns:

1. [What If?](https://www.youtube.com/watch?v=KP3nUQ8XT0s), executed again by *Optimbum*.
2. [Bear Trap Triplets](https://www.youtube.com/watch?v=oef8lhGh3Bg), executed again by *Optimbum*.
3. [Untitled Voodoo Mission](https://www.youtube.com/watch?v=N2fXGfhVy6A), executed by speedrunner *z w*.
4. [The Devil Is In The Details](https://www.youtube.com/watch?v=5wAtRzCUCCw), executed again by *z w*.
5. [Bird Hunting](https://www.youtube.com/watch?v=96om0eFvf0Y), executed again by *z w*

<p class="navigation-link">[Back to Navigation](#navigation)</p><br>




## Conclusion

And that's it! If you made it this far, congratulations! You should have a proud **36 of 36** on your Steam profile 😀 