
# 🚨 ProximityMotionAlert  
*“Beep only when it’s coming at you.”*
---

## What it does
A minimal Arduino sketch that  
1. Reads distance with an HC-SR04 ultrasonic sensor.  
2. Compares the **current** distance with the **previous** one.  
3. Sounds a buzzer **only while an object is moving closer**.  
   Silence resumes when the object stops or retreats.

Perfect for  
- Desk “anti-cat” sentries  
- Reverse-car beepers that ignore stationary obstacles  
- Interactive art that reacts to approaching people

## Hardware
| Part | Pin (default) |
|------|---------------|
| HC-SR04 Trig | D5 |
| HC-SR04 Echo | D18 |
| Active Buzzer | D23 |
| Power | 5 V & GND |

## Quick Start
1. Wire everything according to the table above.  
2. Clone this repo into your Arduino IDE:
   ```bash
   git clone https://github.com/muzahidulislamabir66731011/ProximityMotionAlert.git
   ```
3. Open `ProximityMotionAlert.ino` and upload.  
4. Open the Serial Monitor (115 200 baud) and watch the magic.  
5. Wave your hand toward the sensor—**beep!** Pull back—**silence.**

## Tweak It
| Goal | Change |
|------|--------|
| Faster response | Lower `delay(200)` (minimum 50 ms recommended) |
| Different trigger logic | Swap the comparison operator |
| LED instead of buzzer | Replace `digitalWrite(BUZZER_PIN, …)` with LED pin |


## License
MIT 
## Contributions
Pull-requests welcome:  
- Add a potentiometer for sensitivity  
- Replace buzzer with DFPlayer MP3 module for voice alerts  
- Port to ESP32 & send MQTT “intruder” messages  
…go wild!
```

---

### 🛠️ Next Steps
1. Create the repo on GitHub with the name `ProximityMotionAlert`.  
2. Drop the `.ino` file and the above `README.md` into the root.  
3. Add a 10-second demo GIF/video to the `/assets` folder and embed it.  
4. Tag the first release as `v1.0.0` and add the topics listed earlier for discoverability.
```
Happy hacking!
