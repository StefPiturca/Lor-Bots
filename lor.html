import discord
import random
import json
import os
from discord.ext import commands
from urllib.parse import quote

intents = discord.Intents.default()
bot = commands.Bot(command_prefix="!", intents=intents)

cards = {
    "champions": ["Lux", "Zoe", "Tristana", "Norra", "Caitlyn", "Teemo", "Garen", "Fiora"],
    "spells": ["Single Combat", "Mystic Shot", "Vile Feast", "Starlit Epiphany", "Rummage", "Blazing Salvo", "Deny"],
    "units": ["Mageseeker Investigator", "Petty Officer", "Solari Shieldbearer", "Conductor of Mists", "Stygian Onlooker"],
    "landmarks": ["Sunken Temple", "Bandle City", "The Sun Temple"]
}

predefined_decks = {
    "lux_illuminate": {
        "champions": ["Lux", "Zoe"],
        "spells": ["Mystic Shot", "Single Combat", "Starlit Epiphany", "Starshaping"],
        "units": ["Mageseeker Conservator", "Mageseeker Investigator"],
        "landmarks": ["Sunken Temple"]
    },
    "tristana": {
        "champions": ["Tristana"],
        "spells": ["Mystic Shot", "Rummage", "Deny"],
        "units": ["Bandle Commando", "Petty Officer"],
        "landmarks": ["Bandle City"]
    },
    "norra": {
        "champions": ["Norra"],
        "spells": ["Vile Feast", "Mystic Shot"],
        "units": ["Conductor of Mists", "Petty Officer"],
        "landmarks": ["Sunken Temple"]
    },
    "norra_caitlyn": {
        "champions": ["Norra", "Caitlyn"],
        "spells": ["Mystic Shot", "Vile Feast"],
        "units": ["Conductor of Mists"],
        "landmarks": ["Noxian Control"]
    },
    "teemo": {
        "champions": ["Teemo"],
        "spells": ["Mystic Shot", "Blazing Salvo"],
        "units": ["Bandle Commando", "Stygian Onlooker"],
        "landmarks": ["Bandle City"]
    },
    "garen": {
        "champions": ["Garen"],
        "spells": ["Single Combat", "Righteous Strike"],
        "units": ["Solari Shieldbearer"],
        "landmarks": ["Demacian Justice"]
    },
    "fiora": {
        "champions": ["Fiora"],
        "spells": ["Single Combat", "Deny"],
        "units": ["Solari Shieldbearer"],
        "landmarks": ["The Sun Temple"]
    }
}

def create_deck_link(deck):
    all_cards = deck["champions"] + deck["spells"] + deck["units"] + deck["landmarks"]
    encoded = quote("\n".join(all_cards))
    return f"https://runeterra.ar/deck#custom-deck?deck={encoded}"

def generate_random_deck():
    return {
        "champions": random.sample(cards["champions"], 2),
        "spells": random.sample(cards["spells"], 6),
        "units": random.sample(cards["units"], 8),
        "landmarks": random.sample(cards["landmarks"], 2)
    }

@bot.command(name="roll")
async def roll_deck(ctx, deck_type: str = "random"):
    if deck_type in predefined_decks:
        deck = predefined_decks[deck_type]
        link = create_deck_link(deck)
        await ctx.send(f"**{deck_type.replace('_', ' ').title()} Deck**")
        await ctx.send(f"Deck Link: {link}")
        await ctx.send(f"```json\n{json.dumps(deck, indent=4)}\n```")
    elif deck_type == "random":
        deck = generate_random_deck()
        link = create_deck_link(deck)
        await ctx.send("**Random Deck Generated**")
        await ctx.send(f"Deck Link: {link}")
        await ctx.send(f"```json\n{json.dumps(deck, indent=4)}\n```")
    else:
        await ctx.send("Unknown deck name. Use `!roll random` or one of: `" + "`, `".join(predefined_decks.keys()) + "`")

@bot.command(name="dice")
async def roll_dice(ctx, sides: int = 6):
    result = random.randint(1, sides)
    await ctx.send(f"You rolled a {result} on a {sides}-sided die.")

# Run the bot
TOKEN = os.environ.get("DISCORD_BOT_TOKEN")
bot.run(TOKEN)
