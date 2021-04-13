@client.command()
@commands.has_permissions(administrator=True)
async def gwroll(ctx,messageid,*,prize):
  howmany = 1
  msg = await ctx.fetch_message(messageid)
  reactions = msg.reactions
  winners = []
  for reaction in reactions:
          for i in range(howmany):
                      winners.append(choice(await reaction.users().flatten()))
  winner_mention = ("\n".join([winner.mention for winner in winners]))

  
  await ctx.send(f"Congratulations {winner_mention}, you have won the giveaway for **{prize}**")
