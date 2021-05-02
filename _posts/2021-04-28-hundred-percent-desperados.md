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
    </style>
</head>

I've been replaying [Desperados III](https://store.steampowered.com/app/610370/Desperados_III/) on PC recently. As I was going through the first few missions, I thought *Gee, it sure would be fun to do all these extra badges and maybe even 100% this game!* However, the badges for each mission do not show up until after the first completion, which leads to a ton of wasted time. One also ends up missing a lot of the secret achievements in each mission. Thus, I decided to create this 'roadmap' of sorts to allow one to 100% this game as efficiently as possible.

<h3 style="color: red"> CAUTION! This post contains a lot of spoilers for the main game. </h3>
<br>
<br>

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

Each playthrough section will be coloured <span class="normal-difficulty">like so</span> if the difficulty is 'Normal' and <span class="hard-difficulty">like so</span> if the difficulty is 'Hard'. There will also be farming tips for some of the mission-agnostic achievements, if applicable. For these farming techniques, it suffices to create a quicksave just a second before the event, then reloading this over and over again until the desired number has been reached. For example, if farming for ***Doubletime: Kill 200 guards using Cooper's double shot***, use Showdown mode to make Cooper target two guards, then quicksave, then execute the action. After that, just reload the quicksave and execute it again over and over. Even though you're killing the same guards again and again, it still counts as separate kills in Steam achievements.

<nav>
  <h3 id="navigation">Navigation</h3>
  1. this unordered seed list will be replaced by toc as unordered list
  {:toc}
</nav>

<!-- ## Natural Achievements

All the natural achievements are listed here. Some farming techniques have also been provided in case you're falling short. For all of these techniques, 

<table>
    <colgroup>
      <col span="1" style="width: 30%;">
      <col span="1" style="width: 70%;">
    </colgroup>
    <tr style="text-align: center">
        <th>Achievement</th>
        <th>Farming Technique</th>
    </tr>
    <tr>
        <td><i>Out of Sight, Out of Mind: Hide 250 bodies.</i></td>
        <td>Any mission with all five characters allows one to use Showdown mode to hide six bodies at once (two at a time with Hector).</td>
    </tr>
    <tr>
        <td><i>Maneater Shrub: Hide 750 bodies.</i></td>
        <td>Same as above.</td>
    </tr>
    <tr>
        <td><i>Another One Bites the Dust: Kill 500 guards.</i></td>
        <td>The simultaneous kill of Frank and the circle of guards at the end of <b>The Old and the New</b> is probably the best 'story' location for this. Otherwise, you can place as many guards as you can find on an oil puddle in <b>O'Hara Ranch</b>, set them on fire, and rinse and repeat to batch-complete this achievement.</td>
    </tr>
    <tr>
        <td><i>Someone Call the Undertaker: Kill 1,000 guards.</i></td>
        <td>Same as above.</td>
    </tr>
    <tr>
        <td><i>Watch Out Below!: Kill 50 guards using the environment.</i></td>
        <td>The loose logs at the sawmill in <b>The Bridge at Eagle Falls</b> is likely the best place to do this. Kate's disguise is fairly easy to get and after that walking to the sawmill and triggering the trap is straightforward.</td>
    </tr>
    <tr>
        <td><i>They Wear Red Bandanas: Kill 75 Long Coats.</i></td>
        <td>The Long Coat tutorial at the start of <b>Troublemakers in Flagstone</b> is probably the best location for this.</td>
    </tr>
    <tr>
        <td><i>Damn Good Marksman: Snipe 50 guards with McCoy.</i></td>
        <td>The three guards at the beginning of <b>The Bridge at Eagle Falls</b> are a good candidate for doing both this achievement and <i>Doubleshot</i> at once.</td>
    </tr>
    <tr>
        <td><i>Puppet Master: Mind control 25 guards with Isabelle.</i></td>
        <td>The guard at the start of <b>Louisiana Voodoo</b> is likely the most convenient location for this.</td>
    </tr>
    <tr>
        <td><i>Good Girl: Kill 75 guards with Bianca.</i></td>
        <td>The Bianca tutorial at the start of <b>Troublemakers in Flagstone</b> is probably the best location for this. Note that you do not have to wait for the Bianca animation to finish. Steam will notify you on every twenty-fifth kill.</td>
    </tr>
    <tr>
        <td><i>Doubletime: Kill 200 guards using Cooper's double shot.</i></td>
        <td><b>Byers Pass</b> has multiple good locations for this achievement specifically. Note that you don't have to wait for the guards' shooting animation to finish. Steam will notify you on every twentieth kill.</td>
    </tr>
    <tr>
        <td><i>Follow Me Darling: Make guards follow Kate for 1,000 meters total.</i></td>
        <td><b>Back Alley Jazz</b> is likely the best mission for this since the disguise can be obtained within minutes of starting and there are multiple guards open to repeated luring. Make sure to use the fast-forward functionality to speed this up. Steam will notify you on every fiftieth metre.</td>
    </tr>
</table>

## Specific Achievements -->

This section will focus on the other achievements, proceeding in a mission-by-mission manner. Each mission section will focus on badges (for *Sheriff's Badge: Earn 90 badges.*), [the Mimimi dev NPCs](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement) (for *Seasoned Bounty Hunter: Kill 15 of the hidden Mimimi devs.* and *Veteran Bounty Hunter: Kill 31 hidden Mimimi devs.*), and any secret achievements.

## On The Hunt
This mission has no badges or Mimimi devs, but has a few secret achievements.

<h4 class="normal-difficulty">Playthrough #1</h4>

* Achieve ***[Lindberg and Hutch: Decide the outcome of a duel]("https://www.youtube.com/watch?v=esaBl_teFSI")***.
* Achieve ***[Sorry, Dad!: Knock out your father]("https://www.youtube.com/watch?v=jWd_AASN5QE")***.

<p style="text-align: right; font-size: 12px;">[Back to Navigation](#navigation)</p>




## Byers Pass
This is probably the easiest mission to complete in Desperado difficulty, so the last playthrough will focus on that. At the end of these playthroughs, you should have **7/90** badges.

<h4 class="hard-difficulty">Playthrough #1</h4>

* Achieve ***[The Picnic: Enjoy some cupcakes during a picnic](https://www.youtube.com/watch?v=esaBl_teFSI)***.
* Shoot the first golden chicken for ***[Chicken Dinner: Kill all 3 golden chickens](https://guides.gamepressure.com/desperados-iii/guide.asp?ID=58096)***.
* Earn <u>Save all groups of civilians</u>. This is straightforward, except for the last civilian being interrogated by Big Ann: you must move quickly to kill her before she kills him.
* Achieve ***[Kaboom!: Kill 5 guards at once with dynamite](https://www.youtube.com/watch?v=Ox_FC5DDJ10)*** and earn <u>Kill 3 bandits at the same time</u> at once.
* Earn <u>Kill 10 bandits using dynamite</u>. Just make sure to leave enough guards alive for this by the end.
* Earn <u>Distract 3 bandits at the same time using Cooper's coin</u> by tossing a coin at the three bandits standing under the big rock.
* Earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.
* [Optional] Farm for ***Doubletime: Kill 200 guards using Cooper's double shot*** and ***Damn Good Marksman: Snipe 50 guards with McCoy***.

<h4 class="normal-difficulty">Playthrough #2</h4>

* Earn <u>Don't save during the mission</u>. You can explicitly set the number of saves to 'None' in the difficulty options if you reflexively save like I do 😂. Go slowly and ensure that you can safely proceed. It's not the end of the run if you trigger an alert however: just wait it out.
* Earn <u>Don't use firearms</u>. This is fairly straightforward. Rely on McCoy's `Bag` and Cooper's `Knife`. Note that for pairs, Cooper can use `Knife` on one guard and immediately `Knockout` the other.

<h4 style="color:purple">Playthrough #3</h4>
* Achieve ***Hardcore: Finish a mission on "Desperado" difficulty*** by completing this mission in 'Desperado' difficulty.

<p style="text-align: right; font-size: 12px;">[Back to Navigation](#navigation)</p>




## Troublemakers in Flagstone
At the end of these playthroughs, you should have **14/90** badges.

<h4 class="hard-difficulty">Playthrough #1</h4>

* Earn <u>Make the deaths of 4 targets look like accidents</u>. To do so, poison Wild Marge, provoke the bull to kill Jarvis, drop the church bell onto The Duke, and drop the incomplete building wall onto McBane.
* Earn <u>Bury Josh</u>. In the church area, there's a NPC named "Josh". After killing him, throw him into the open grave in the church courtyard to earn this.
* Earn <u>Listen in on 10 private conversations</u>. The various conversations are marked by comic-book speech bubbles.
* Earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.
* Kill the [two Mimimi developer NPCs](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement).

<h4 class="normal-difficulty">Playthrough #2</h4>

* Earn <u>Kill 3 mission targets at the same time</u>. This is a little finnicky, but not overly so. You must poison Wild Marge, and then, the moment her mission indicator becomes green, kill two others. I killed McBane and The Duke with Cooper's dual `Revolvers` from the top of the cliff near the church, but there are alternate methods. Note that this will set of an alert, but you can just wait for it to clear up and then re-enter the civil zone.
* Earn <u>Don't kill or knock out anyone in the train track area</u>. This doesn't apply to McBane, in case you were wondering.
* Earn <u>Don't touch any bushes or haystacks</u>. This isn't as hard as it sounds. Approach Wild Marge's building from the right, and Jarvis' area from the left.

<p style="text-align: right; font-size: 12px;">[Back to Navigation](#navigation)</p>




## Until Death Do Us Part
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

<p style="text-align: right; font-size: 12px;">[Back to Navigation](#navigation)</p>



## O'Hara Ranch
This mission has a pretty straightforward [speedrun strategy](https://www.youtube.com/watch?v=TYcpPkJNkAk), executed by speedrunner *Optibum*. Thus, the speedrun badge will be included. At the end of these playthroughs, you should have **27/90** badges.

<h4 class="hard-difficulty">Playthrough #1</h4>
This is the non-speedrun playthrough. In any case, try to follow the same route to get a feel for it.

* Earn <u>Kill all Long Coats</u>. **Important!** While this badge is self-explanatory, it must be done *before* you get McCoy and Hector to the rooftop for the second part of the level.
* Earn <u>Finish the mission without using a torch</u>. Note that even picking up a torch counts as 'using' it. You can shoot enemies carrying lanterns over oil puddles to light them instead.
* Earn <u>Win the bet with Hector</u>. If you're paranoid, you can switch McCoy to non-lethal mode.
* Earn <u>Burn 15 guards in oil puddles</u>. This can be 'manually' done by knocking out 15 guards and using Hector and McCoy to place them on an oil puddle, then lighting it on fire. Make sure to do one set of five to achieve*** Inferno: In the first part of the mission, burn 5 guards at once with oil traps***.
* Achieve ***[M-M-M-M-MONSTER KILL: Kill 6 guards at once using only a single skill](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement)*** by placing some knocked-out guards in a pile and then using Hector's `Sawed-off` on them.
* Earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.
* Kill the [two Mimimi developer NPCs](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement).
* [Optional] Farm for ***Good Girl: Kill 75 guards with Bianca***.

<h4 class="normal-difficulty">Playthrough #2</h4>
This is the speedrun playthrough.

* Earn <u>Win the bet with McCoy</u>. The speedrun route relies heavily on McCoy, so you should earn this naturally.
* Earn <u>Speedrun: complete the mission in under 17:00 minutes</u>. Make sure you have adequately memorized what each character is supposed to do. Play smoothly and calmly; 17 minutes is more than enough time for this route. Optimbum makes some risky plays to avoid waiting for guard rotations, but you can afford to wait for them.

<p style="text-align: right; font-size: 12px;">[Back to Navigation](#navigation)</p>




## The Bridge at Eagle Falls
At the end of these playthroughs, you should have **33/90** badges.

<h4 class="hard-difficulty">Playthrough #1</h4>

* Earn <u>Get the dynamite from the quarry</u>. I feel the quarry is easier to deal with on Hard difficulty than the shooting range.
* Earn <u>Kill 3 guards at the same time in a quarry explosion</u>. This is easy to do on the way to the previous badge. Note that the explosion is instantaneous, so you can run and detonate it if needed.
* Earn <u>Kill 5 guards when destroying the bridge</u>. To do this, place 5 unconscious guards on the section of the bridge just above where the dynamite goes. During the cutscene, this part will fall away and you'll receive the badge.
* Achieve ***Goodbye Colorado: Blow up a bridge*** and earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.
* Kill the [two Mimimi developer NPCs](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement).

<h4 class="normal-difficulty">Playthrough #2</h4>

* Earn <u>Get the dynamite from the shooting range</u>.
* Earn <u>Kill 3 guards with rolling logs</u>. The logs are near the sawmill adjacent to the shooting range. With her Disguise, Kate can easily walk there and release the logs undetected.
* [Optional] Farm for ***Follow Me Darling: Make guards follow Kate for 1,000 meters total***.

<p style="text-align: right; font-size: 12px;">[Back to Navigation](#navigation)</p>




## One Good Shot
This mission has no badges or secret achievements, but has a single Mimimi dev.

<h4 class="normal-difficulty">Playthrough #1</h4>

* Kill the [Mimimi developer NPC](https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement).

<p style="text-align: right; font-size: 12px;">[Back to Navigation](#navigation)</p>




## One Hell of a Night
<table>
    <colgroup>
      <col span="1" style="width: 15%;">
      <col span="1" style="width: 85%;">
    </colgroup>
    <tr>
        <td><i>Badges</i></td>
        <td>
            After this mission, we will have <b>36/90</b> badges.
            <ol>
                <li><u>Return the money to the bank</u>: <b>Important!</b> This is an easy badge to lock yourself out of. At the very start of the mission, use Hector to knock out the woman outside the hut. She'll drop the money, which Hector can pick up. Drop this onto the floor of the bank in the same room where McCoy is being held to get the badge. If you wait until after you rescue McCoy, she will disappear and the badge will no longer be obtainable.</li>
                <li><u>Free Doc before waking up the others</u>: This is easier than is appears; see the <i>Notes</i> section for details.</li>
                <li><u>Don't use a disguise</u>: This is easier than is appears; see the <i>Notes</i> section for details.</li>
                <li><u>Kill 6 guards</u>: You can throw guards into the water to kill them. You can also kill up to 3 guards using the cannon in the middle of the level.</li>
                <li><u>Don't use the bank's backdoor</u>: The 'back door' refers to the entrance from the construction area. Again, this is easier than it appears; see the <i>Notes</i> section for details.</li>
                <li><u>Make a guard follow your footprints for 50 meters</u>: This requires a bit of timing, but can be done immediately at the very beginning of the level. Lure the guard near the water tower. Use the incline the hut is on to break his line of sight, and keep circling around the cliff until the badge notification appears.</li>
                <li><u>Complete the mission on Hard difficulty</u>: Self-explanatory.</li>
            </ol>
        </td>
    </tr>
    <tr>
        <td><i>Mimimi devs</i></td>
        <td><a href="https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement">Three</a></td>
    </tr>
    <tr>
        <td><i>Secret achievements</i></td>
        <td>
            <a href="https://www.youtube.com/watch?v=9-tsCaqHAOM"><i>Need a Dentist?: Find a patient for the dentist.</i></a>
        </td>
    </tr>
    <tr>
        <td><i>Notes</i></td>
        <td>
            <ul>
                <li><b>Important!</b> This is a general tip, but makes this level extremely easy. A knocked-out and tied up guard will lure <i>any enemy</i> (yes, even Ponchos and Long Coats). Furthermore, they will <i>not</i> sound the alarm until after they untie the guard. This can be abused beyond belief in this level and makes Hector very overpowered; in fact, all 7 badges listed can be done in a <i>single</i> playthrough. This 'mechanic' is a by-product of the NPC AI, and has been <a href="https://www.youtube.com/watch?v=QupN4qDG3Oc">acknowledged by the developers</a> as something which can be abused.</li>
                <li>I noticed that McCoy's bag had somehow dropped, despite McCoy himself not being conscious. I'm not sure if this is a bug or not.</li>
                <li>If you return the money before waking up Kate, her dialog still plays even though she's unconscious.</li>
            </ul>
        </td>
    </tr>
</table>


### Louisiana Voodoo
<table>
    <colgroup>
      <col span="1" style="width: 15%;">
      <col span="1" style="width: 85%;">
    </colgroup>
    <tr>
        <td><i>Badges</i></td>
        <td>
            After this mission, we will have <b>41/90</b> badges.
            <ol>
                <li><u>Don't touch water</u>: This badge is quite tedious, but is probably easier than the alternative <u>Don't use Isabelle's connect ability</u>, since Connect is so integral to Isabelle's playstyle. Note that this doesn't just mean you can't swim; a single <i>touch</i> of water invalidates this badge. Thus, keep checking the status regularly to make sure that no character accidentally walked through a puddle or something somewhere.</li>
                <li><u>Free Kate or Hector first</u>: Note that neither can be freed without the key; since McCoy isn't available, the lock cannot be picked.</li>
                <li><u>Kill 5 guards at the same time</u>: This is best done after you have Hector and Cooper, at the least. Hector's shotgun and Cooper's double-shot make this fairly easy.</li>
                <li><u>Kill 3 guards with an environment kill</u>: This is straightforward. At the very beginning, the mind-controlled guard can be used to kill the two guards under the pile of boxes. After that, there's a single guard under a big rock near Cooper's boat.</li>
                <li><u>Complete the mission on Hard difficulty</u>: Self-explanatory.</li>
            </ol>
        </td>
    </tr>
    <tr>
        <td><i>Mimimi devs</i></td>
        <td><a href="https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement">Two</a></td>
    </tr>
    <tr>
        <td><i>Secret achievements</i></td>
        <td>
            <a href="https://guides.gamepressure.com/desperados-iii/guide.asp?ID=58096"><i>Chicken Dinner: Kill all 3 golden chickens.</i></a>
        </td>
    </tr>
    <tr>
        <td><i>Notes</i></td>
        <td>
            <ul>
                <li><b>Important!</b> This is a general tip for all levels with Isabelle. If a normal guard and a Long Coat are connected together, <i>killing or knocking out</i> the normal guard will cause the Long Coat to enter the stagger state, as if they'd been shot. This allows Isabelle to single-handedly take out Long Coats. This can be exploited further by bringing along one unconscious and tied-up guard and connecting to them.</li>
                <li>Note that Isabelle cannot move when she's mind-controlling someone. This means you must move her to a safe place before starting, otherwise you run the risk of another guard seeing her.</li>
                <li>Isabelle can use a mind-controlled guard to easily take over the Gatling gun near Cooper's boat and clear the area.</li>
            </ul>
        </td>
    </tr>
</table>


### Back Alley Jazz
<table>
    <colgroup>
      <col span="1" style="width: 15%;">
      <col span="1" style="width: 85%;">
    </colgroup>
    <tr>
        <td><i>Badges</i></td>
        <td>
            After this mission, we will have <b>47/90</b> badges.
            <ol>
                <li><u>Don't kill any suspects</u>: This badge is fairly straightforward. It's best combined with badges #4 and #5.</li>
                <li><u>Kill all suspects</u>: Again, fairly straightforward. It's best combined with badge #3. If doing so, make sure to save at least 2 mind-control darts for use with the dog.</li>
                <li><u>Kill 3 guards using dogs</u>: You must mind-control the dog and force it to bite a guard. You will need at least 2 darts for this. Make sure to use Isabelle to connect two guards together to get more bang for you bark 😉. Similar to mind-controlled guards, other enemies will not raise an alert upon seeing the dead bodies.</li>
                <li><u>Don't kill anyone</u>: This is a little tedious, but not overly difficult; see the <i>Notes</i> section. Make sure to switch all characters to their non-lethal mode by default to avoid mistaken kills.</li>
                <li><u>Get information on aliases and locations for all suspects - Gather the codenames and locations for all suspects</u>: This does not need to be done if going for badge #2.</li>
                <li><u>Complete the mission on Hard difficulty</u>: Self-explanatory.</li>
            </ol>
        </td>
    </tr>
    <tr>
        <td><i>Mimimi devs</i></td>
        <td><a href="https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement">Three</a></td>
    </tr>
    <tr>
        <td><i>Secret achievements</i></td>
        <td>None</td>
    </tr>
    <tr>
        <td><i>Notes</i></td>
        <td>
            <ul>
                <li><b>Important!</b> This is a general tip for all levels with Kate. Kate has an 'instantaneous' body pick up animation. This can be used to cancel the long falling animation of guards who have just been shot. For example, if a guard is standing in the grey viewcone of another guard, Kate can shoot him and them immediately pick them up to cancel the fall animation and prevent the other guard from noticing. This makes certain parts of this level much easier.</li>
                <li>Make sure to get Kate's disguise; it's very easy to obtain and her Lure ability can be heavily used in this level. Luring guards from guarded zones to civilian zones is especially useful since most actions such as knockouts and kills are ignored in civil zones. The pier section specifically can be almost completely cleared with disguised Kate alone.</li>
                <li>When wearing her disguise, Kate will not get caught even if she triggers environmental traps.</li>
            </ul>
        </td>
    </tr>
</table>


### Burn the Queen
<table>
    <colgroup>
      <col span="1" style="width: 15%;">
      <col span="1" style="width: 85%;">
    </colgroup>
    <tr>
        <td><i>Badges</i></td>
        <td>
            After this mission, we will have <b>53/90</b> badges.
            <ol>
                <li><u>Kill everyone except for civilians</u>: This badge is fairly straightforward. Make sure to not knock out, tie up, and throw guards into bushes; if they disappear, this badge will become unobtainable. Note that this badge also (apparently) includes the reinforcements that arrive after you set the boat on fire; use Hector's shotgun to deal with them the moment they exit the guard house.</li>
                <li><u>No knockouts or melee kills except for Isabelle</u>: This isn't as difficult as it sounds; you're still allowed to use Cooper's knife and guns, Hector's bear trap, and McCoy's sniper rifle. In fact, it's possible to forgo even his sniper rifle and combine this with badge #3.</li>
                <li><u>Don't use McCoy's snipe</u>: This includes using McCoy's sniper rifle to shoot environmental objects and to stun Long Coats.</li>
                <li><u>Open all cages</u>: Very easy to do, especially when combined with badge #1.</li>
                <li><u>Hide all bodies in bushes, wells, houses, etc.</u>: Self-explanatory. Best combined with badge #1.</li>
                <li><u>Complete the mission on Hard difficulty</u>: Self-explanatory.</li>
            </ol>
        </td>
    </tr>
    <tr>
        <td><i>Mimimi devs</i></td>
        <td><a href="https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement">Two</a></td>
    </tr>
    <tr>
        <td><i>Secret achievements</i></td>
        <td>None</td>
    </tr>
    <tr>
        <td><i>Notes</i></td>
        <td>
            <ul>
                <li>Breaking the oil barrel will not cause an alert, so you can do this part at your leisure.</li>
                <li>Cooper can single-handedly kill a Long Coat by shooting him three times with his revolvers.</li>
            </ul>
        </td>
    </tr>
</table>


### Dirt and Blood
<table>
    <colgroup>
      <col span="1" style="width: 15%;">
      <col span="1" style="width: 85%;">
    </colgroup>
    <tr>
        <td><i>Badges</i></td>
        <td>
            After this mission, we will have <b>59/90</b> badges.
            <ol>
                <li><u>Choose the path on the left</u>: This badge cannot be done simultaneously with badge #2. Note that the 'path' isn't locked until any character reaches the last stretch of street before the meeting point.</li>
                <li><u>Choose the path on the left</u>: Same as above.</li>
                <li><u>Don't use a disguise</u>: This is easier than it looks.</li>
                <li><u>Kill 3 guards using the steamer wheel</u>: The steamer wheel environmental trap is in the pier on the left path. On Hard difficulty, 3 guards are already in the path of the wheel. Hence, it's best to combine this with badges #6, #3, and #1.</li>
                <li><u>Kill all Long Coats.</u>: Self-explanatory.</li>
                <li><u>Complete the mission on Hard difficulty</u>: Self-explanatory.</li>
            </ol>
        </td>
    </tr>
    <tr>
        <td><i>Mimimi devs</i></td>
        <td><a href="https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement">Two</a></td>
    </tr>
    <tr>
        <td><i>Secret achievements</i></td>
        <td>None</td>
    </tr>
    <tr>
        <td><i>Notes</i></td>
        <td>
            <ul>
                <li>If you're feeling particularly masochistic, you can try doing one of badge #1 and #2 alongside <u>Don't use any of Cooper's skills</u> and the other badges to finish all 6 badges in a single playthrough.</li>
                <li><b>Important!</b> This is a general tip for all levels with Hector. Hector can use bodies to knock out your <i>other</i> characters, then pick them up and throw them over short obstacles. In levels like these where piles of boxes and head-height fences block of multiple paths, this can be used to essentially 'skip' section of the level, or tackle them from behind.</li>
            </ul>
        </td>
    </tr>
</table>


### A Cart Full Of Gunpowder
<table>
    <colgroup>
      <col span="1" style="width: 15%;">
      <col span="1" style="width: 85%;">
    </colgroup>
    <tr>
        <td><i>Badges</i></td>
        <td>
            After this mission, we will have <b>65/90</b> badges.
            <ol>
                <li><u>Traverse the mine on the left side</u>: This badge cannot be done simultaneously with badge #2. Note that the 'path' isn't locked until any character reaches the second-to-last section of the map i.e. the bit just after the river area (from the left) and after the multilevel mine area (from the right).</li>
                <li><u>Traverse the mine on the right side</u>: Same as above.</li>
                <li><u>Don't pick up the dynamite</u>: This is easier than it looks; you don't have to kill everybody in the upper parts of the last section since they're too high up to see the track area.</li>
                <li><u>Kill 20 opponents with dynamite</u>: Another easy and really fun badge which makes the entire last section of the map very quick. Once you get your hands on the dynamite, go crazy; the barrel is unlimited.</li>
                <li><u>Don't use Isabelle's connect ability</u>: This is actually easier that it looks, especially if combined with badge #4. The first three sections of the level are fairly straightforward even without connect.</li>
                <li><u>Complete the mission on Hard difficulty</u>: Self-explanatory.</li>
            </ol>
        </td>
    </tr>
    <tr>
        <td><i>Mimimi devs</i></td>
        <td><a href="https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement">Two</a></td>
    </tr>
    <tr>
        <td><i>Secret achievements</i></td>
        <td>None</td>
    </tr>
    <tr>
        <td><i>Notes</i></td>
        <td>
            <ul>
                <li>If you're up for a challenge, you may want to combine <u>Pick up only McCoy's gear</u> along with one of badges #1 and #2, and badges #4 and #5; Isabelle's connect is part of her gear. On the route to 90 badges, this will allow you to get one less badge in the other levels.</li>
            </ul>
        </td>
    </tr>
</table>
<p style="text-align: right; font-size: 12px;">[Back to Navigation](#navigation)</p>

### A Captain Of Industry
This mission actually has a normal-difficulty [speedrun strategy](https://www.youtube.com/watch?v=UovLY9SbneY) that is very simple to execute. By making small tweaks here and there to this route, you can very easily earn all eight badges inside 30 minutes.

<h4 class="normal-difficulty">Playthrough #1</h4>
Follow the route in the speedrun video linked above, with a small change to earn an extra badge.

* Earn <u>Don't use both distractions</u>; this is automatically achieved by this route.
* Earn <u>Don't let anyone see you</u>. The 22 minutes for the speedrun badge is more than enough to execute this route. Thus, take your time and avoid being spotted.
* Earn <u>Use mind control on Devitt's character</u>; this is automatically achieved by this route. Note that some online guides say that this badge cannot be earned unless one of the distractions has been used and DeVitt is alone with his men - this is **false** (at least as of writing this post); you can get it at any point.
* Earn <u>Kill 2 guards with a statue</u>. Immediately after relinquishing mind-control on DeVitt and securing him, use Hector to drop the statue in the courtyard onto the guard and the Long Coat. If you miss a rotation, don't worry; you have enough time to do this and still get the speedrun badge.
* Earn <u>Speedrun: Complete the mission in under 22:00 minutes</u>. Make sure you have memorized everything that each character has to do. Play smoothly and calmly; you have enough time. The last section is a little finnicky; I found that connecting a few guards and then using `Stella` on them helps.

<h4 class="hard-difficulty">Playthrough #2</h4>
Follow the same route as earlier, but with more substantial changes. If you didn't get the speedrun badge, I recommend trying again in normal mode and doing this playthrough without time pressure. Make sure to make a **manual save** before finishing this playthrough; continue reading for more details.

* Earn <u>Don't touch any bushes or haystacks</u>. Follow the same route as earlier, but make sure to not touch any bushes or haystacks. This makes Isabelle and Hector's section slightly more complicated.
* Earn <u>Don't use any of Kate's or Cooper's skills</u>. This is easier than it looks, since neither of them actually do much on this route. Substitute Cooper's kills with Isabelle and `Connect`, and Kate's `Perfume` with `Stella`. Note that Cooper's tying up of a unconscious person counts as a 'skill'. Both Kate and him can still carry bodies, however. In the last section, use Hector and Isabelle to kill all guards and knock out all civilians.
* Earn <u>Complete the mission on Hard difficulty</u> by completing this playthrough.
* Once you've earned the three badges above, reload your **manual save** and backtrack with Cooper to kill the two [Mimimi developer NPCs]("https://www.trueachievements.com/a298714/veteran-bounty-hunter-achievement") at the very beginning of the level.

<p style="text-align: right; font-size: 12px;">[Back to Navigation](#navigation)</p>

> This post is in progress! Check back soon.