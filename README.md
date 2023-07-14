# Tgbot_FootballGame
Just simple football game in TgBot


    @dp.message_handler(text="/football")
    async def cmd_football(message: types.Message):
        await message.answer("Let`s play football!")
        await sleep(0.5)
        await message.answer("First attempt:")
        user_1 = await message.answer_dice('⚽️')
        user_1data = user_1["dice"]['value']
        await sleep(5)
    
        if 5 > user_1data > 2:
            await message.answer("GOAL!!!")
        elif user_1data == 5:
            await message.answer("Increadible goal!!!")
        else:
            await message.answer('Past the gate')
        await sleep(1)
    
        await message.answer('Second attempt:')
        user_2 = await message.answer_dice('⚽️')
        user_2data = user_2["dice"]['value']
        await sleep(5)
        if 5 > user_2data > 2:
            await message.answer("GOAL!!!")
        elif user_2data == 5:
            await message.answer("Increadible goal!!!")
        else:
            await message.answer('Past the gate')
        await sleep(1)
    
        await message.answer("Last attempt:")
        user_3 = await message.answer_dice('⚽️')
        user_3data = user_3["dice"]['value']
        await sleep(5)
        if 5 > user_3data > 2:
            await message.answer("GOAL!!!")
        elif user_3data == 5:
            await message.answer("Increadible goal!!!")
        else:
            await message.answer('Past the gate')
        await sleep(1)
        await message.answer(f"You got {user_3data + user_2data + user_1data}/15 points")
