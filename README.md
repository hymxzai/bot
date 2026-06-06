import discord
from discord.ext import commands
import os
from pystyle import Colorate, Colors
import json
import random
import asyncio


token = "MTEzMjQ1Njg2ODYzMjA4NDU2Mg.GJp-bB.PSV7iJKLRpTGRqsEf2Th-1PKLf5PWjXugpedrc"  # ← PASTE YOUR VALID USER TOKEN HERE


bot = commands.Bot(command_prefix='.', self_bot=True, help_command=None)



@bot.event
async def on_ready():
    total_friends = 0  # Bots cannot access friends list

    clear_cmd()

    print(Colorate.Horizontal(
        Colors.red_to_yellow,
        "Selfbot Started\n"
    ))

    logo(bot.user.name, total_friends)


def clear_cmd():
    os.system('cls' if os.name == 'nt' else 'clear')


def logo(username, total_friends):
    logo_art = f"""
'            /$$                             
'           | $$                             
'  /$$   /$$| $$$$$$$   /$$$$$$$  /$$$$$$$   
' |  $$ /$$/| $$__  $$ /$$_____/ /$$_____/   
'  \  $$$$/ | $$  \ $$| $$      | $$         
'   >$$  $$ | $$  | $$| $$      | $$         
'  /$$/\  $$| $$$$$$$/|  $$$$$$$|  $$$$$$$   
' |__/  |__/|_______/  \_______/ \_______/   
|   
                                Logged in as = {username} 
"""

    print(Colorate.Vertical(Colors.red_to_yellow, logo_art))


@bot.check
async def globally_allow_self(ctx):
    return True




import discord
from discord.ext import commands



@bot.command()
async def help(ctx):
    msg = await ctx.send("```[XBCC SYSTEM] Loading help menu... 0%```")

    frames = [
        "```[XBCC SYSTEM] Loading help menu... 10%```",
        "```[XBCC SYSTEM] Loading help menu... 25%```",
        "```[XBCC SYSTEM] Loading help menu... 45%```",
        "```[XBCC SYSTEM] Loading help menu... 65%```",
        "```[XBCC SYSTEM] Loading help menu... 85%```",
        "```[XBCC SYSTEM] Decrypting modules... 99%```",
        "```[XBCC SYSTEM] ACCESS GRANTED ✔```",
    ]

    for frame in frames:
        await asyncio.sleep(0.7)
        await msg.edit(content=frame)

    await asyncio.sleep(0.5)

    help_text = (
        "```yaml\n"
        "━━━━━━━━━━ XBCC CONTROL PANEL ━━━━━━━━━━\n\n"
        " SYSTEM\n"
        "  help | ping | server | invite\n\n"
        " INFO\n"
        "  userinfo | pfp | banner | snipe\n\n"
        " FUN\n"
        "  coinflip | roll | dice | gay | smart\n\n"
        " STATUS & TOOLS\n"
        "  playing | watching | listening | streaming\n"
        "  removepresence | voice | spam\n\n"
        " BYPASS\n"
        "  status | dm | timeoutall | untimeoutall | leaveallgroups | banall\n"
        "  purge | cleardm | nuke | deleteroles | createchannels |  deletechannels | clone\n\n"
        "━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\n"
        "```"
... (1,257 lines left)
