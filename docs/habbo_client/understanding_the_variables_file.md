---
layout: default
title: Understanding the variables file 
parent: Habbo Client
has_children: false
nav_order: 1
---
# Understanding the variables file

The following section specifically covers the `external_vars.txt` AKA variables file used for the v14/v15 of the oldschool shockwave Habbo client. 


Typical variables file sorted alphabetically 
```
cast.entry.1=hh_interface
cast.entry.2=hh_patch_uk
cast.entry.3=hh_people_1
cast.entry.4=hh_people_2
cast.entry.5=hh_shared
cast.entry.6=hh_entry
cast.entry.7=hh_messenger
cast.entry.8=hh_registrat
cast.entry.9=hh_kiosk_room
cast.entry.10=hh_room_utils
cast.entry.11=hh_human
cast.entry.12=hh_furni_classes
cast.entry.13=hh_room
cast.entry.14=hh_club
cast.entry.15=hh_photo
cast.entry.16=hh_entry_au
cast.entry.17=hh_navigator
cast.entry.18=hh_purse
cast.entry.19=hh_buffer
cast.entry.20=hh_dynamic_downloader
cast.entry.21=hh_recycler
cast.entry.22=hh_soundmachine
cast.entry.23=hh_poll
char.conversion.mac=[128:219,130:226,131:196,132:227,133:201,134:160,13 5:224,136:246,137:228,139:220,140:206,145:212,146: 213,147:210,148:211,149:165,150:208,151:209,152:24 7,153:170,155:221,156:207,159:217,161:193,165:180, 167:164,168:172,170:187,171:199,172:194,173:208,17 4:168,176:161,180:171,182:166,183:225,184:252,186: 188,187:200,191:192,192:203,193:231,194:229,195:20 4,196:128,197:129,198:174,199:130,200:233,201:131, 202:230,203:232,204:237,205:234,206:235,207:236,20 9:132,210:241,211:238,212:239,213:205,214:133,216: 175,217:244,218:242,219:243,220:134,223:167,224:13 6,225:135,226:137,227:139,228:138,229:140,230:190, 231:141,232:143,233:142,234:144,235:145,236:147,23 7:146,238:148,239:149,241:150,242:152,243:151,244: 153,246:154,247:214,248:191,249:157,250:156,251:15 8,252:159,255:216]
client.version.id=401
client.window.title=Ninja Hotel
club.subscription.disabled=0
dynamic.download.name.template=hof_furni/hh_furni_xx_%typeid%.cct
dynamic.download.samples.template=sound/%typeid%.cct
dynamic.download.url=http://localhost/v14/
external.figurepartlist.txt=http://localhost/v14/figuredata.txt
fuse.project.id=habbo_uk
image.library.url=http://localhost/c_images/
interface.cmds.active.ctrl=["move","rotate"]
interface.cmds.active.owner=["move","rotate","pick","delete"]
interface.cmds.item.ctrl=[]
interface.cmds.item.owner=["pick"]
interface.cmds.photo.ctrl=[]
interface.cmds.photo.owner=["pick","delete"]
interface.cmds.user.ctrl=["kick","friend","ignore","trade","unignore","userpage"]
interface.cmds.user.friend=["friend","ignore","trade","unignore","userpage"]
interface.cmds.user.owner=["take_rights","give_rights","kick","friend","ignore","trade","unignore","userpage"]
interface.cmds.user.personal=["badge","dance","wave","hcdance","userpage"]
interstitial.max.displays=5
language=en
link.format.userpage=http://www.habbo.fi/home/%ID%/id/
moderator.cmds=[":alert x",":ban x",":kick x",":superban x",":shutup x",":unmute x",":transfer x",":softkick x"]
navigator.private.default=4
navigator.public.default=3
navigator.visible.private.root=4
navigator.visible.public.root=3
paalu.key.list=[#bal1:"Q", #bal2:"E", #push1:"A", #push2:"D", #move1:"N", #move2:"M", #stabilise:"SPACE"]
permitted.name.chars=1234567890qwertyuiopasdfghjkl zxcvbnm-=?!@:.,
permitted.password.chars=1234567890qwertyuiopasdfg hjklzxcvbnm-=?!@:.,
purse.transactions.active=1
room.cast.1=hh_people_small_1
room.cast.2=hh_people_small_2
room.cast.3=hh_cat_code
room.cast.4=hh_cat_gfx_all
room.cast.5=hh_pets_common
room.cast.6=hh_pets
room.cast.7=hh_soundmachine
room.cast.private=["hh_room_private"]
room.cast.small.1=hh_pets_50
room.default.floor=101
room.default.wall=101
stats.tracking.javascript.template=http://secure-dk.imrworldwide.com/cgi-bin/m?ci=Habbohotel&cg=0&si=\TCODE
stats.tracking.javascript=url
struct.font.bold=[#font:"vb",#fontSize:9,#lineHeight:10,#color:rgb(" #000000"),#ilk:#struct,#fontStyle:[#plain]]
struct.font.italic=[#font:"v", #fontSize:9,#lineHeight:10,#color:rgb("#000000"),# ilk:#struct,#fontStyle:[#italic]]
struct.font.link=[#font:"v", #fontSize:9,#lineHeight:10,#color:rgb("#000000"),# ilk:#struct,#fontStyle:[#underline]]
struct.font.plain=[#font:"v", #fontSize:9,#lineHeight:10,#color:rgb("#000000"),# ilk:#struct,#fontStyle:[#plain]]
struct.font.tooltip=[#font:"v", #fontSize:9,#lineHeight:10,#color:rgb("#000000"),# ilk:#struct,#fontStyle:[#plain]]
swimjump.key.list=[#run1:"A", #run2:"D", #dive1:"W", #dive2:"E", #dive3:"A", #dive4:"S", #dive5:"D", #dive6:"Z", #dive7:"X", #jump:"SPACE"]
```

> Taken from [Quackster V14 Zip](https://github.com/Quackster/Kepler/blob/master/tools/Quackster_v14.zip) /v14/external_vars.txt

## cast.entry.[number]
`cast.entry.[number]` is a variable used for telling the client to load external .CCT files (cast files). 

These files will be loaded from the same directory from where `habbo.dcr` is being loaded from. 

## char.conversion.[machineType]
`char.conversion.[machineType]` is a variable used within the inner workings of `fuse_client.cct` specifically `String Services Class`. It's used for mapping characters between platforms. Most likely for fonts. 

## client.version.id
Default `1` (Anything goes)

`client.version.id` is used within the `hh_entry.cct` which is where most of the login logic is handled. It specifically used when the client initiates the method `startSession` which only happens if the client to server communication is encrypted which most likely isn't the case for you if you're using Kepler. 

Were Kepler to have encryption enabled and the `client.version.id` is not the same on the server-side it will prompt the client with text `alert_old_client` which is defined in the `external_texts`. 

## client.window.title
Default `Habbo Hotel`

Will set the window title if the client is launched via Shockwave projector. 

## club.subscription.disabled
Default: `0|1`

Determines whether to allow the users to subscribe to Habbo Club within the client.

## dynamic.download.url
Default: `http://localhost/v14/`

This is the base URL for downloading various things like furni and sounds.

## dynamic.download.name.template
Default: `hof_furni/hh_furni_xx_%typeid%.cct`

The directory to load furni from. 

## dynamic.download.samples.template
Default: `sound/%typeid%.cct`

The directory to load sounds from. Specifically used for loading in the Trax sounds.  

Full URL will be a combination of `dynamic.download.url` and `dynamic.download.samples.template`.

## external.figurepartlist.txt
Default: `http://localhost/v14/figuredata.txt`

This is a url for the text file containing the figure part mapping. This is where the mapping of figures(cloth, skin, etc) is being mapped together then used within the client.

## fuse.project.id
Development variable. Used in combination with `quickLogin`. 

## image.library.url
default: `http://localhost/c_images/` | `http://images.habbohotel.com/c_images/`

This variable is used for loading catalogue images and badges not found in the cast files. 

If the client is unable to find the catalogue header or teaser image it will try and load the image from the provided url constructed in the following manner:

`{image.library.url}/catalogue/{headerImgName|teaserImg}_{language}.gif`

## interface.cmds.[objType].[ctrlType]
Buttons shown depending on objType and ctrlType. E.g. Room owners are being shown `interface.cmds.active.owner` for when `objType` equal to `active` and `ctrlType` equal to `owner`.

## interstitial.max.displays
Default: `5`

Amount of ads to show in a session or so it seems based on the code. 

Requires further fiddling to understand usage.

## language
Default: `en`

Used when loading catalogue images from the server. 

See `image.library.url`

## link.format.userpage
Default: `http://www.habbo.fi/home/%ID%/id/`

Link for the Habbo home link used in the infostand and messenger. 

## moderator.cmds
List of chat commands that will be taking a username as the second input. E.g. `:kick Wizter`.



## navigator.private.default
Default: `navigator.visible.private.root`

Determines the default category for private rooms.

As you can see the default variable is equal to another variable. This is true but can be overwritten. 

## navigator.public.default
Default: `navigator.visible.public.root`

Determines the default category for public rooms.

As you can see the default variable is equal to another variable. This is true but can be overwritten. 

## navigator.visible.private.root

Determines the default category for private rooms.

## navigator.visible.public.root

Determines the default category for public rooms.

##  paalu.key.list
Default: `[#bal1:"Q", #bal2:"E", #push1:"A", #push2:"D", #move1:"N", #move2:"M", #stabilise:"SPACE"]`

The keys used for WobbleSquabble. 

## permitted.name.chars
Default: `1234567890qwertyuiopasdfghjkl zxcvbnm-=?!@:.,`

As the variable hints this is the permitted characters allowed in a username during registration. 

## permitted.password.chars
Default: `1234567890qwertyuiopasdfg hjklzxcvbnm-=?!@:.,`

As the variable hints this is the permitted characters allowed in a password during registration. 

## purse.transactions.active
Default: `0|1`

Determines whether to allow the user to see a list of transactions within the Habbo wallet. 

## room.cast.[number]
Cast loaded when entering a room. 

## room.cast.private
Cast loaded when joining a private room.

## room.cast.small.[number]
Casts loaded for small rendered rooms, like large public rooms, large private rooms.

## room.default.floor
Default: `203`

Default floor color palette id. Found in `hh_room_private.cct`.

## room.default.wall
Default: `201`

Default wall color palette id. Found in `hh_room_private.cct`.

## stats.tracking.javascript.template
This is not required.

Tracking url. This URL will be called from time to time to save analytics. 

**Don't use this if you're using Shockwave projector to run the Habbo Client. This will cause Internet Explorer to open.**

## stats.tracking.javascript
This is not required. 

**Don't use this if you're using Shockwave projector to run the Habbo Client. This will cause Internet Explorer to open.**

## struct.font.[fontStyle]
 
Determines the font style. 

## swimjump.key.list
Default: `[#run1:"A", #run2:"D", #dive1:"W", #dive2:"E", #dive3:"A", #dive4:"S", #dive5:"D", #dive6:"Z", #dive7:"X", #jump:"SPACE"]`

Controls for the Lido tower jump. 

## navigator.updatetime
How often the navigator should refresh. 

## purse.valuefield.active 
Tells whether to show the value of the credits in the transaction log within the wallet. 


