WELCOME BOT WITH SLASH COMMANDS FOR DISCORD.PY

This source code allows you to welcome members while having Slash commands work. Now has support where you can
set up the bot for the Welcome module to work properly in multiple servers like what you see in bots like Dyno, Carl bot, etc
Meaning you can set up a welcome channel per server and it will welcome members in each server seperatly just like popular bots like Dyno.
Making this version more advanced then the last version.
No need to make a bunch of discord bots and hosting them seperatly anymore for each server

Includes:
- Sending messages in a desired text channel (New version now supports having one bot in multiple servers and welcomes members in your desired set channel for each server.)
- Gives an unverified role to a member with verification command
- Sends a welcome message to a webhook
- DMs members upon joining the server
- Slash commands working with all of this.

================================================

REQUIREMENTS:
- Knowledge of Discord.py
- A discord bot application with token (with Server Members intent enabled)
- Python 3.8.6 or newer (Using a Python software version below this version may have a chance to cause issues or errors)

================================================

SETUP:
1. Fork or Download this Source code to your hosting provider (or computer if you wish to self-host it)
2. Create a Discord Bot Application and copy your bot token at https://discord.com/developers
3. At the bottom, replace DISCORDBOTTOKEN with your Discord bot token you just created.
4. Enable the Server Members intent in the developers portal. Should also unselect "Public Bot" in the developers portal as well.
5. MODIFICATIONS:
- At webhook = Webhook.from_url('WEBHOOKTOKEN', adapter=AsyncWebhookAdapter(session)), replace WEBHOOKTOKEN with the Webhook url (if you want the webhook)
- At mutedRole = discord.utils.get(ctx.guild.roles, name="ROLENAMEHERE"), replace ROLENAMEHERE with the name of the role you want the bot to give in your server.
6. Install discord.py and discord-py-slash-command
7. Run the bot (I advise you test with an alt or with a friend to ensure you did everything correctly)

You need to do nothing with the .json file. That file is already set to go.

SET UP BOT ON DISCORD.
1. Invite the bot to your server.
2. Use /setwchannel command to change which text channel you want the welcome message to be sent to.
3. Create an "Unverified" role and channel for new members to use the /verify command. If needed, run /verifysetup. To ensure no errors, give your bot admin.
4. Repeat Steps 1-3 for each server you want your bot it.
NOTE: The bot will not DM new members if you do not set up the role the bot gives unless you want to modify the code. However, you must know what you are doing.

================================================

NOTE: This source code was designed to be made for private utility bots in a few servers.
You could have this a public bot but can not guarente proper working results.

If your bot stays unverified and enabled the Message Content intent, you may be able to use regular commands
instead.

DISCLAIMER: THERE IS LITERALLY NO WARRENTY IF YOU DECIDE TO USE THIS SOURCE CODE. IF YOU DECIDE TO USE
THIS SOURCE CODE, IT IS TO BE USED AT YOUR OWN RISK! WE WILL NOT BE HELD LIABLE FOR ANY DAMAGES WHAT SO EVER!

READ THIS: I am unable to get a data reset command to work at all.
The only way to remove your server/channel ids from the json file is too manually remove it from the file.
Turn on Developers mode to find out your server id.
I tried modifing the on_guild_remove in https://stackoverflow.com/questions/64760333/how-to-set-a-welcome-channel-discord-py
and modified it to a command but unable to get it to work. At this point, idk if it is even possible to remove data from your json file via command.
I always get the following error: discord.ext.commands.errors.CommandInvokeError: Command raised an exception: KeyError: 'MYGUILDIDHERE'
If you know how to fix this or create a data reset command, PLEASE let me know but submitting an issue or pull request.

===============================================

CREDITS:
https://stackoverflow.com/questions/64760333/how-to-set-a-welcome-channel-discord-py
This help page is how I learned this.