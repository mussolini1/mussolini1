import discord
import random
# from discord.ext import commands
from discord.ext.commands import Bot


pat_list = ["word1", "word2", "word3", "word4"]
hit_list = ["http://surl.li/bepwc", "http://surl.li/bepwd", "http://surl.li/bepwg"]
kiss_list = ["word1", "word2", "word3", "word4"]

random_hit = random.choice(hit_list)

bot = Bot(command_prefix=".")


@bot.event
async def on_ready():
    print(f"{bot.user} Ready to Work! ")
    await bot.change_presence(activity=discord.Game("Mincraft"))
    #

@bot.command()
async def sendpepe(ctx):
    emb = discord.Embed(title="Pepe!", colour=discord.Colour.dark_green())
    emb.set_image(url="http://surl.li/bcpqz")
    await ctx.send(embed=emb)

@bot.command()
async def test(ctx):
    emb = discord.Embed(title="Test", colour=discord.Colour.dark_green())
    emb.set_image(url="http://surl.li/bboqo")
    await ctx.send(embed=emb)

@bot.command()
async def mitaka_inst(ctx):
    emb = discord.Embed(title="MiTaka", colour=discord.Colour.dark_green())
    emb.set_image(url="#")
    await ctx.send("Link")

@bot.command()
async def mitaka_yt(ctx):
    emb = discord.Embed(title="MiTaka", colour=discord.Colour.dark_green())
    emb.set_image(
        url="https://yt3.ggpht.com/ytc/AKedOLStSjBQ8lMWzCTFcLT1sTQ_RiMCtd8dkyI-YvWb=s88-c-k-c0x00ffffff-no-rj")
    await ctx.send(" https://www.youtube.com/channel/UCINfD63ocXyCM-CSspOD44A ")

@bot.command()
async def mitaka_vk(ctx):
    emb = discord.Embed(title="MiTaka", colour=discord.Colour.dark_green())
    emb.set_image(url="#")
    await ctx.send("Link")

@bot.command()
async def surprise_for_mitaka(ctx):
    print(f"{ctx.author.mention} Митакааааааа желаю тебе 100мл подписчиков твой канал растет не по дням а по часам! ")
    await ctx.send("https://www.instagram.com/p/CYmQz_zNK8S/")

@bot.command()
async def hit(ctx, member: discord.Member = None):

    await ctx.channel.send(f"{random_hit}" f"{ctx.author.mention} Ударил-ла {member.mention}")
    # await ctx.channel.send(f"{random_hit}")


