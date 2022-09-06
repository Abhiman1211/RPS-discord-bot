# RPS-discord-bot
## Purpose
<br>
This is an interactive bot that plays rock, paper and scissors and actively communicates. Our purpose was to explore different modules of python and also make learning them intresting by constructing this fun game.
<br>

## Python modules
<br>
1. Random: Random module helps in choosing the one of the three options rock, paper and scissor randomly
<br>
2. Discord: Discord pyhton module revolves around the concept of events. An event is something you listen to and then respond to. For example, when a message happens, you will receive an event about it that you can respond to.
<br>

## Documentation

import discord<br>
import random<br>
from discord.ext import commands<br>

bot = commands.Bot(command_prefix=".")<br>


@bot.event<br>
async def on_ready():<br>
    print("Let's get started!")<br>


@bot.command()<br>
async def hello(ctx):<br>
    await ctx.reply('Hello!')<br>


@bot.command()<br>
async def rps(ctx, message):<br>
    answer = message.lower()<br>
    choice = ["rock", "paper", "scissors"]<br>
    computers_answer = random.choice(choice)<br>
    if answer not in choice:<br>
        await ctx.reply("This is not a valid choice. Choose one of these: rock, paper, scissors.")<br>
    else:<br>
        if computers_answer == answer:<br>
            await ctx.reply("It's a tie :/.")<br>
        if computers_answer == "rock":<br>
            if answer == "paper":<br>
                await ctx.reply(f"You win! I chose {computers_answer} and you chose {answer}!")<br>
        if computers_answer == "rock":<br>
            if answer == "scissors":<br>
                await ctx.reply(f"You loose! I chose {computers_answer} and you chose {answer}!")<br>
        if computers_answer == "paper":<br>
            if answer == "rock":<br>
                await ctx.reply(f"You loose! I chose {computers_answer} and you chose {answer}!")<br>
        if computers_answer == "paper":<br>
            if answer == "scissors":<br>
                await ctx.reply(f"You win! I chose {computers_answer} and you chose {answer}!")<br>
        if computers_answer == "scissors":<br>
            if answer == "rock":<br>
                await ctx.reply(f"You win! I chose {computers_answer} and you chose {answer}!")<br>
        if computers_answer == "scissors":<br>
            if answer == "paper":<br>
                await ctx.reply(f"You loose! I chose {computers_answer} and you chose {answer}!")<br>

bot.run('OTMwMzU2NDk4NjAzODQ3NzMw.Yd0sAg.hD8J5UTjQ58XoPB36YW83Z-LnV8')<br>
## RPS bot <br>
![image](https://user-images.githubusercontent.com/96763019/188546779-66583fce-a325-4420-bd53-05c4c74c1ed8.png)
<br>

<br>

## TEAM MEMBERS
<br>
1.)<a href="https://github.com/Abhiman1211">Abhiman Gautam </a>
<br>
2.)<a href="https://github.com/Riya1929">Riya Gandhi </a>
<br>
3.)<a href="https://github.com/zankhana46">Zankhana Mehta </a>
<br>
