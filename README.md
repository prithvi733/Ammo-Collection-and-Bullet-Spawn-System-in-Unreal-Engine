# Ammo-Collection-and-Bullet-Spawn-System-in-Unreal-Engine
# 🎯 Aim:
To implement a gameplay feature where the player collects ammo pickups in the game world. Upon collecting ammo, the player's ammo count increases, enabling more bullet spawns (shots).

# 🛠️ Procedure:
1. Setup Player Character
.Open your PlayerCharacter Blueprint.
.Add a new Integer variable named AmmoCount.
.Set an initial default value (e.g., AmmoCount = 10).
.Ensure you have a shooting mechanism in place that uses AmmoCount to determine if a bullet can be fired.

2. Create Ammo Pickup Blueprint
.Go to the Content Browser → Right-click → Blueprint Class → Select Actor → Name it BP_AmmoPickup.
.Add components:
 *Static Mesh: Representing the ammo (e.g., a bullet or crate).
 *Sphere Collision: To detect overlap with the player.
.In the Event Graph of BP_AmmoPickup:
 *Use OnComponentBeginOverlap on the Sphere Collision.
*Cast to PlayerCharacter.
*Increase the player’s AmmoCount (e.g., AmmoCount += 5).
*Optionally, play a pickup sound or effect.
*Destroy the ammo pickup actor.
3. Update Shooting Logic (Optional)
.In your player’s shooting logic:
 *Before spawning a bullet, check if AmmoCount > 0.
.If true:
 *Spawn bullet.
 *Decrease AmmoCount by 1.
4. Place Ammo in the World
.Drag instances of BP_AmmoPickup into your level from the Content Browser.
.Adjust position, mesh, and pickup range as needed.

# Output:
![image](https://github.com/user-attachments/assets/99d3d6e7-1d29-488e-8d05-d698427fdcd3)

![image](https://github.com/user-attachments/assets/a3ba25ea-880f-44ac-96ac-93aac7f7008e)

![image](https://github.com/user-attachments/assets/3cabb356-81eb-4336-9a16-1337dd9e655a)

![image](https://github.com/user-attachments/assets/4a07ee0a-7003-46f4-adbf-36d29809ee5f)

# Result:
.The player starts with a limited number of bullets.
.When the player overlaps with an ammo pickup:
 *The ammo is collected.
 *The player's AmmoCount increases.
.The player can now fire additional bullets based on the updated ammo count.


