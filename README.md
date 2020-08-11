# Bot setup: PluralKit
the name of the bot is **PluralKit**, and you can get the bot [here](https://pluralkit.me/). 
<br><blockquote>this bot has many different uses, but i've specifically used it to streamline social media notifications for **BTS** in discord.</blockquote>

*(note: the creator of the bot does explain how to set up the bot on their [page](https://pluralkit.me/start/), 
but they’ve used it under a different context, so i figured since we all want the same things here i can just teach you how i’ve set up the bot for my net!)*

tl;dr basically what this bot does is it creates a __system__, where you can host multiple profiles/members  of your choosing in one place. 

<blockquote>keep in mind that there are also alternatives and you don't have to use it if you'd rather not, because it does require some members in the net to
actively keep up with all of BTS's social media pages and not a lot of people have the time to do that. 

<br>this is just a deliberate choice made on our end to use this bot as we can have everything under one belt instead of having multiple bots in one server. </blockquote>

## Content
* [Part i](#Part-i)
  * [Setting Up](#Setting-Up)
  * [Adding Profiles](#Adding-Profiles)
  * [Customise Profiles](#Customise-Profiles)
* [Part ii](#Part-ii)
  * [Proxy Tags](#Proxy-Tags)
  * [Link Accounts](#Link-Accounts)
  * [End](#End)
* [Commands](#Commands)
* [Alternatives](#Alternatives)

## Part i: 
### Setting Up

1. before you start, it’s best to have already have a rough idea/number of how many profiles you want to host. 
in my case, we have **6 profiles: the 3 bts twitter accounts, instagram, vlive, and weverse.**


<blockquote>sidenote: maybe think about the channels you want to run these profiles in. there’s no additional setup required, 
it’s done manually so you can always change it up according to your preference. this will just be easier for you for later. 
the way we've set it up is having 6 different channels for each profile, just for reference.</blockquote>

2. once that’s done, you can set up the system with the command `pk;system new [the name of your choice]` on discord.  

as an example, 
```
pk;system new BTS 
```

3. once you have that, you can use the command  `pk;system` to check the status of your system. 

### Adding Profiles
now that we have a system, we can start adding the profiles (see #1 on [Setting Up](#Setting-Up)).

1. add a profile with `pk;member new [name]`. to make my life easier, i've just named the profiles according to their official pages. 
```
pk;member new bts_twt
pk;member new bts_bighit
pk;member new bighitent
```
  * repeat the steps for each profile you have.
   * keep in mind that this should reflect the number of profiles you want to post/want your net members to stay updated about, 
   so since for my net we’ve decided on 6 profiles, there should be 6 names once i’ve finished setting up the profiles. 
   if you’ve decided on 3, then there should be 3, and vice versa.
   
<blockquote> think of this as a set username for your profile/member moving forward, so it should be kept simple so it's easy to remember.</blockquote>
   
2.  you can check your profiles with this command `pk;system name list full`.

### Customise Profiles
this is the part where you customise the display names, avatar, description, etc of your profiles.

* for display names: `pk;member <member> displayname [display name]`
  ```
  * eg. pk;member bts_twt displayname bts_twt
        pk;member btsvlive displayname BTS on vlive
  ```
  *  **note:** the display name is what will be shown when you post.
  
* for avatars: `pk;member <member> avatar [url|@mention]`
  ```
  * eg. `pk;member bts_twt avatar [uploads image of the icon of your choosing in the same message]`
  ```
  
## Part ii
### Proxy Tags
<blockquote>(ok now we're at the complicated part, but i’ll try to make it painless for you)</blockquote>

the idea of proxy tags here works similarly to a command tag where you can use it to post under the name of the bot. to set this up, use the command: 
```
pk;member [member] proxy [add|remove] [example proxy]
```

so coming from that, i'll use bts_twt as an example. it'll look like:
```
pk;member bts_twt proxy add btstwt:text
```
where  `btstwt:text` is my `[example proxy]`, a.k.a. my chosen proxy tag. *the `[example proxy]` text is entirely up to you to decide, 
you don't have to follow what i've done here.

for example, when a member posts under their bts_twt account, the command will be `bts_twt:text`, and the `text` part is where you replace it with
the *actual* text in a tweet/caption.
here, i'll copy the caption and the link* to the tweet and in the channel, i'll write:
```
btstwt:#Dynamite 
https://twitter.com/BTS_twt/status/1292855794430427136
```
and press enter.
<blockquote>*it depends on how you want to format the tweet in discord, this is just an example of how we do it.</blockquote>

once it's done, **PluralKit** will automatically convert it to look like a bot has sent out the message:
```
bts_twt [BOT]
#Dynamite 
https://twitter.com/BTS_twt/status/1292855794430427136
```

that's pretty much for tags! you will then repeat the same process to all of the profiles that you have.

### Link Accounts
once you have all the profiles set up with it's proxy tags, 
one last thing you need to do is to link *discord accounts* to the system so a user is given permission to use the command,
or else PluralKit won't be able to detect the command.
* whoever set up the bot will use the command below to allow users to use it.

```
pk;link [@account]
eg. pk;link @username#4220
```

you can check the linked accounts by using
```
pk;system
```

### End
yay you're done! that's how it is to set up this bot, 
and because it's a little complicated i've opted to use github to host it because the formatting workds better imo~ 


## Commands
a list of important commands if you're using this bot for the same purpose as i do.

Commands | Description
---------- | ------
pk;member <member>                   |  Looks up information about a member.
pk;member <member> rename <new name> |  Renames a member
pk;member <member> proxy [add/remove] [example proxy] | Changes, adds, or removes a member's proxy tags
pk;member <member> delete | Deletes a member
pk;member <member> description [description] | Changes a member's description
pk;member <member> avatar [url/@mention] | Changes a member's avatar
pk;system [system] list [full] | Lists a system's members
pk;link <account> | Links this system to a different account.

For a full list of commands, you can find it [here](https://pluralkit.me/commands).
