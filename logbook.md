# Spider Robot - My Error Log

I built a quadruped spider robot. 4 legs, 12 servos. Here is everything that went wrong and what I learned from each problem.

---

## Error 1: The Power Problem

**What happened:** The servos kept twitching randomly. Sometimes they wouldn't move at all. I thought my code was wrong.

**What was actually wrong:** I used an LM2596 step-down module to control the voltage. I didn't check it with a multimeter before connecting everything. The module was still at factory settings, outputting only 4V instead of the 7V the servos needed.

**How I fixed it:** After hours of frustration, I finally tested the voltage with a multimeter. Saw 4V. Adjusted the module to output 7V. Servos came to life.

**What I learned:** Always check your power supply with a multimeter before connecting anything else. Trust no factory setting.

---

## Error 2: The Loose Joints

**What happened:** The legs felt wobbly. The robot couldn't hold its position. It kept sagging.

**What was actually wrong:** The screws and nuts I had were not the perfect size for the 3D printed parts where the femur connects to the leg. Everything fit, but there was extra space. The joints were loose.

**How I fixed it:** I didn't fully fix this one. I tried wrapping threads with tape to fill the gap. It helped a little but not completely. Next time I will buy the exact sizes before starting.

**What I learned:** Mechanical fit matters as much as code. Loose joints mean an unstable robot.

---

## Error 3: The Servo Horn Problem

**What happened:** The servo horns kept slipping or popping out of position during movement. The robot would suddenly drop a leg.

**What was actually wrong:** The 3D printed parts I used had gaps that were slightly too big for the servo horns. Nothing fit snugly.

**How I fixed it:** I tried hot glue. It worked temporarily but failed under stress. I tried tape. Same problem. This one is still not fully solved.

**What I learned:** 3D prints are not always precise. Test fit before assembling everything.

---

## Error 4: The Dead Leg (Still Not Fixed)

**What happened:** One leg - the front right - does not set into position. Instead of bending like the others, one of its servos stretches straight vertically as soon as I turn on the power.

**What I tried so far:**
- Swapped the servo with a working one from another leg → same problem, so not the servo
- Checked wiring multiple times → looks fine
- Tested different code values → nothing changed
- Measured voltage at that leg → same as others

**What I think might be wrong:** Maybe signal interference? The wires to that leg are longer than the others because of how I arranged things. Or maybe the Arduino pin itself is damaged. I don't have an oscilloscope to test signal quality.

**Status:** Still broken. Still trying.

**What I learned from this failure:** Debugging is not linear. Sometimes you try everything and still don't know the answer. That's okay. You keep going.

---
## Error 5: The Soldering Disaster

**What happened:** I needed to solder connections for the stepdown module and power supply. I had never soldered before.

I bought a 60W soldering iron because it was cheap. BIG MISTAKE.

I tried soldering the wires to the stepdown module. The iron was too hot. I burned the module. Completely destroyed it. Smoke came out. Had to throw it away.

**What I learned the hard way:** 60W is too powerful for small electronics work. It heats up too fast and transfers too much heat. It will burn components before you even realize what happened.

**How I fixed it:** I bought a 30W soldering iron instead. Much better for small work.

I also bought flux and watched tutorials on how to use it properly. Learned that flux helps the solder flow and stick to the right places. Without flux, solder just balls up and falls off.

**What I learned:** 
- Use the right tool for the job. 30W iron for electronics, not 60W.
- Flux is not optional. It makes soldering actually work.
- Practice on old wires before soldering your actual project.
- Soldering is a skill. You have to learn it like anything else.

**Aftermath:** The second step-down module is soldered correctly. No burns. Clean joints. Works perfectly.

## Summary of What I Learned

| Problem | Lesson |
| :--- | :--- |
| Voltage drop | Check power with a multimeter before anything else |
| Loose screws | Get the right part sizes before building |
| Horn gaps | 3D prints need test fitting |
| Dead leg | Some problems take a long time to solve |
| Burned module with 60W iron | Use 30W iron for electronics. Learn soldering before using it. |

