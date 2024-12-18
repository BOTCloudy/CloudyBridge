> [!IMPORTANT]  
> You Need To Activated Beta API On Your Minecraft World.  
> Follow Step By Step On This New Repository. 

# 🌩️ CloudyBridge

Welcome To **CloudyBridge** Add-On Integration For Your Minecraft Java And Bedrock Dedicated Server! This Guide Will Walk You Through The Steps To Get Your Server Connected With Our Bot And Manage Your Community Effectively.

## 🚀 Features

- **Premium Access**: Unlock Premium Features By Registering With Our Bot.
- **Group Management**: Set Up Your Admin And Forum Groups Effortlessly.
- **Minecraft Add-On**: Seamlessly Integrate Your Server With Cloudy WhatsApp Bot.

## 📋 Getting Started

To Get Started With CloudyBridge, Follow These Steps:

1. **Register For Premium Access**:  
   Contact Our Bot At `+62 851-7986-2199` To Register For Premium Access And Unlock The Full Potential Of CloudyBridge.
   Use `?premium` Command And Send Message.

2. **Set Up Groups**:  
   You Will Need To Create Two Groups: An **Admin Group** And A **Forum Group** Whatever Its Name. Invite The Bot To These Groups Via `/join linkGroup` Command.

   <img src="https://github.com/user-attachments/assets/11a7a46d-4ca2-4817-97cd-3e82e6f351e7" width="250px">

3. **Initialize Groups**:

   - Initialize **Admin Group** First `/mc init admin`.
   - Then, Initialize **Forum Group** `/mc init forum`.
  
    <img src="https://github.com/user-attachments/assets/25fef158-6103-4545-9649-40c1e5dc6459" width="250px">  <img src="https://github.com/user-attachments/assets/64320ae2-d19d-4fc0-9aa1-bbe9024a9cd6" width="250px">

4. **Generate An Auth Code**:
   Generate Authentication Code In Admin Group Using `/mc auth putSomeRandomText` Commands.
   
   <img src="https://github.com/user-attachments/assets/c939f5c4-89af-49ad-9b0c-6d1fa7ff4690" width="250px">

5. **Download Add-On**:  
   Go To [Releases](https://github.com/BOTCloudy/CloudyBridge/releases) Section Of This Repository, Download Minceraft Add-On `jar For Java` And `zip For Bedrock`.

6. **Configure Server**:
      
      For Java:
      
      - You Can Just Drop `CloudyBridge.jar` File Into `plugins` Folder, And Start Your Server.
      - Once Server Is Started, Go To `CloudyBridge` In `plugins` Folder, And Edit `config.yml`. 
      
      ```yaml
      #Server Config
      server: ""  # Server ID From Admin Group Initialization
      auth: ""  # Auth Code That You Already Set From Admin Group
      whitelist: [] # Allow Specific GT To Use In-Game Command, Ex: ["fankyfankz","Wverrr"]
      
      #Default Config
      prefix: "!"  # Prefix Custom Command
      gt: "§3§l<CLOUDY> §r§b"  # Custom GT For Command Reply
      join: "§b§lSilahkan Gabung Ke Group Untuk Bermain.\n§r§ehttps://chat.whatsapp.com/qwerty123"  # Notification When Member Isn't Register
      banned: "§4§lKamu Sudah Dibanned."  # Notification When Member Has Been Banned
      joinTimeout: 60  # Number In Seconds, How Long Will It Take For Unregistered Players To Play Trial On Your Server
      bannedTimeout: 10  # Number In Seconds How Long Does It Take To Kick Banned Players On Your Server
      reasonIn: "§r§6-> "  # Custom Sign For In-Game Reason
      reasonOut: "§r§e-> "  # Custom Sign For Reason When Trying To Join
      theEndOpen: "20.00 31/12/2024"  # Format: HH.mm DD/MM/YYY, Ex: "20.00 31/12/2024"
      theEndNotification: "The End Belum Dibuka Hingga Waktu Yang Telah Ditetapkan"  # Notification For The End
      spawn: "0 64 0" # Default Spawn Point X Y Z
      ```
           
      For Bedrock:
      
      - Extract `CloudyBridge.zip`
      - Navigate To `scripts` Folder And Edit The `config.js` File.
      - Match Server ID And Auth Code You Generated Earlier In The Admin Group.
      
      ```javascript
      export default {
         "server": "", // Server ID From Admin Group Initialization
         "auth": "", // Auth Code That You Already Set From Admin Group
         "whitelist": [], // Allow Specific GT To Use In-Game Command, Ex: ["fankyfankz","Wverrr"]
         
         "prefix": "!", // Prefix Custom Command
         "gt": "§3§l<CLOUDY> §r§b", // Custom GT For Command Reply
         
         "join": "§b§lHay @gt, Silahkan Gabung Ke Group Untuk Bermain.\n§r§ehttps://chat.whatsapp.com/qwerty123", // Notification When Member Isn't Register
         "banned": "§4§l@gt Kamu Sudah Dibanned.", // Notification When Member Has Been Banned
         
         "joinTimeout": 60, // Number In Seconds, How Long Will It Take For Unregistered Players To Play Trial On Your Server
         "bannedTimeout": 10, // Number In Seconds How Long Does It Take To Kick Banned Players On Your Server
         
         "reasonIn": "§r§6-> ", // Custom Sign For In-Game Reason
         "reasonOut": "§r§e-> ", // Custom Sign For Reason When Trying To Join
         
         "theEndOpen": "20.00 31/12/2024", // Format: HH.mm DD/MM/YYY, Ex: "20.00 31/12/2024"
         "theEndNotification": "The End Belum Dibuka Hingga Waktu Yang Telah Ditetapkan", // Notification For The End
         "spawn": "default", // Default Player Spawn Event When The End Is Closed, Format: X Y Z, Default Value: 0 64 0, Ex: 100 -58 100

         "playerId": true, // Log Player ID
         "coorJoin": true, // Log Player Coordinates On Join Event
         "coorLeave": true // Log Player Coordinates On Leave Event
      }
      ```
      
      - Move `CloudyBridge` Folder Into Your `behavior_packs` Directory.
      - Go To Root Folder `worlds\<WorldName>\` And Open `world_behavior_packs.json`, If You Didn't See This, Just Create By That Names.
      - Add CloudyBridge Pack ID 
      
      ```javascript
      [
         {
            "pack_id": "807735f8-8cbb-4915-a33a-d771d68abc02",
            "version": [0,0,0]
         }
      ]
      ```
      
      - Again, Go To Root Folder `config\default\permissions.json` And Add `@minecraft/server-net`
      
      ```javascript
      {
         "allowed_modules": [
            "@minecraft/server-gametest",
            "@minecraft/server",
            "@minecraft/server-ui",
            "@minecraft/server-admin",
            "@minecraft/server-editor",
            "@minecraft/server-net"
         ]
      }
      ```
      
      - Last One, Go To Root Folder And Open `server.properties`, Add `op-permission-level=4` To Gain Highest Role Level For OP, OP Will Be Able To Use Custom Command.
      
      ```javascript
      op-permission-level=4
      ```

7. **Start Your Server**:  
   Start Your Minecraft Dedicated Server, And You Should See A Notification In The Console `[Scripting] </> REST Server Online` That Everything Is Set Up Correctly.

## 🔒 Securing Your Server

- **Enable allowlist**:  
  Secure Your Server By Using `/mc allowlist` Command And Set Status To `true`.
  
  ![4 3](https://github.com/user-attachments/assets/ac25875e-2da5-4274-9a8e-a94544a024a7)

- **Member Registration**:  
  Instruct Your Members To Register On Your Server Using `/mc reg` Command. Once Registered, They Can Join And Play.

  ![5 3](https://github.com/user-attachments/assets/b1a5b430-14f4-49fb-9041-488821b12654)

- **Ban/Unban Members**:  
  If Any Member Becomes Annoying Or Violates Your Rules, Use `/mc ban` Command To Ban Them. If You Wish To Allow Them Back, Use `/mc unban` Command.
  
  ![7 3](https://github.com/user-attachments/assets/7f9d99dc-3fb4-4be4-878f-4114b9183511)

- **Execute In-Game Commands**:  
  You Can Execute Any In-Game Command Via Cloudy WhatsApp Bot, Making Server Management Easier.

  <table style="border-collapse: collapse; width: 100%;">
  <tr>
    <td style="border: none; vertical-align: middle;">
      <img src="https://github.com/user-attachments/assets/07086c43-ed19-4da0-8dd8-c6fa6e1e6a10" height="500px" alt="Image 1">
    </td>
    <td style="border: none; vertical-align: middle;">
      <img src="https://github.com/user-attachments/assets/ce5c289b-013a-4a75-b79f-1bcba7380579" height="400px" alt="Image 2">
    </td>
  </tr>
  </table>
  
## 🌐 Setting Server Status

The Last Step Is To Configure Your Server's IP/Domain And Port Using `/mc server` To Retrieve Server Status Updates Using `/mc status` Without Any Parameter.

 <img src="https://github.com/user-attachments/assets/4adeba20-f496-4118-958f-b1d0342a31eb" width="250px">

## 📜 Extra Custom Commands 
> [!NOTE]  
> 🤖 _Commands Can Only Be Accessed Using BOT_

| Command                                    | Description                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| `list` 🤖 | Show Lists Of Online Players. |
| `reg` 🤖 | User Registration To Play On The Server When allowlist is Enabled.|
| `allowlist <true/false>` | Enable Or Disable allowlist. |
| `allowlist add <GameTag> <User:Optional>` | Add A Game Tag To allowlist. Not Recomended To Use, Instead Of Using `reg` Via Bot. |
| `allowlist remove <GameTag/User>` | Remove Game Tag From allowlist. |
| `ban <GameTag/PlayerID/User> <Reason:Optional>` | Ban Specific Game Tag, Player ID, Or User. Optional Reason Can Be Provided. |
| `unban <GameTag/PlayerID/User> <Reason:Optional>` | Unban Specific Game Tag, Player ID, Or User. Optional Reason Can Be Provided. |
| `mute <GameTag/PlayerID/User> <Time>` | Restrict Player From Sending Message. |
| `unmute <GameTag/PlayerID/User>` | Allow Player To Send Message. |
| `kick <GameTag/PlayerID/User> <Reason:Optional>` | Kick Specific Game Tag, Player ID, Or User. Optional Reason Can Be Provided. |
| `player` | Find Player Information Using Game Tag, Player ID, Or User. |
| `inventory` | Check Player Inventory Using Game Tag, Player ID, Or User. |
| `ender` | Check Player Enderchest Using Game Tag, Player ID, Or User. |
| `coor` | Check Player Coordinates Using Game Tag, Player ID, Or User. |
| `equip <GameTag/PlayerID/User>` | Check Player Equipments Using Game Tag, Player ID, Or User. |
| `lang <en/id>` | Set Your Language To English Or Indonesian. |
| `stats` | Check TPS And Entity. |
| `database` | Show Player Database. |
| `config` | Show / Set Internal Config Depends On Key And Value. |
| `reset <config/player>` | Reset CloudyBridge Database. |
| `cloudy` | Release Version. |

## ✅ Example Usage: 🚫 Ban

#### ✏️ Game Tag With Spacing

- **Via Bot**:  
  `/mc ban "Zoexaka YT" You're Too Overpowered`
  
- **Via In-Game Command**:  
  `!ban "Zoexaka YT" You're Too Overpowered`

#### ✏️ Game Tag With No Spacing

- **Via Bot**:  
  `/mc ban Hyruua You're Too Overpowered`
  
- **Via In-Game Command**:  
  `!ban Hyruua You're Too Overpowered`

#### ✏️ You Can Also Use Player ID Or User Number

Instead Of Using A Game Tag, You Can Ban Or Unban Users By Their Player ID Or User Number If Available.

## 🎉 Enjoy!

You're All Set! Enjoy Managing Your Minecraft Server With CloudyBridge Add-On And Cloudy WhatsApp Bot. If You Encounter Any Issues Or Have Questions, Feel Free To Reach Out.
