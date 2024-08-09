    if gift_value == 1:
        play_sound_web("./sounds/bruit-de-pet.wav")

    elif gift_value == 5:
        play_sound_web("./sounds/bruit_de_rot.wav")

    elif gift_value == 10:
        play_sound_web("./sounds/ouais_cest_greg.wav")

    elif gift_value == 15:
        play_sound_web("./sounds/je_suis_bien.wav")

    elif gift_value == 20:
        play_sound_web("./sounds/alerte_au_gogole.wav")

    elif gift_value == 30:
        play_sound_web("./sounds/quoicoubeh.wav")

    elif gift_value == 49:
        play_sound_web("./sounds/my_movie.wav")

    elif gift_value == 55:
        play_sound_web("./sounds/on_sen_bat_les_couilles.wav")

    elif gift_value == 88:
        play_sound_web("./sounds/chinese_rap_song.wav")

    elif gift_value == 99:
        await control_multiple_relays({"girophare": devices["girophare"]}, "on")
        play_video_web('./videos/alerte-rouge.mp4')
        play_sound_web(f"./sounds/nuke_alarm.wav")
        await asyncio.sleep(8)
        await control_multiple_relays({"girophare": devices["girophare"]}, "off")

    elif gift_value == 100:
        play_video_web('./videos/cri-de-cochon.mp4')

    elif gift_value == 150:
        play_video_web('./videos/rap-contenders-thai.mp4')

    elif gift_value == 169:
        play_video_web('./videos/tu-vas-repartir-mal-mon-copain.mp4')

    elif gift_value == 199:
        await control_multiple_relays({"girophare": devices["girophare"]}, "on")
        play_sound_web(f"./sounds/police-sirene.wav")
        play_sound_web(f"./sounds/fbi-open-up.wav")
        await asyncio.sleep(10)
        await control_multiple_relays({"girophare": devices["girophare"]}, "off")

    elif gift_value == 200:
        play_video_web('./videos/tu-vas-repartir-mal-mon-copain.mp4')

    elif gift_value == 299:
        play_video_web('./videos/alien.mp4')
        play_sound_web(f"./sounds/alien.wav")

    elif gift_value == 398:
        play_video_web('./videos/got-that.mp4')

    elif gift_value == 399:
        play_video_web('./videos/cat.mp4')
        play_sound_web(f"./sounds/nyan_cat.wav")

    elif gift_value == 400:
        play_video_web('./videos/teuf.mp4')
        play_sound_web(f"./sounds/losing-it.wav")

    elif gift_value == 450:
        play_video_web('./videos/mr-beast-phonk.mp4')

    elif gift_value == 500:
        play_sound_web(f"./sounds/oui_oui.wav")
        await control_multiple_relays({"bulles": devices["bulles"]}, "on")
        play_video_web('./videos/oui-oui.mp4')
        await asyncio.sleep(10)
        await control_multiple_relays({"bulles": devices["bulles"]}, "off")

    elif gift_value == 699:
        controller.send_command(SMOKE_MACHINE_URL)
        controller.send_command(SMOKE_TWO_MACHINE_URL)
        play_sound_web(f"./sounds/la_danse_des_canards.wav")
        play_video_web('./videos/cygne.mp4')

    elif gift_value == 899:
        controller.send_command(SMOKE_MACHINE_URL)
        controller.send_command(PINGPONG_MACHINE_URL)
        await control_multiple_relays({"spots": devices["spots"]}, "on")
        play_video_web('./videos/train.mp4')
        play_sound_web(f"./sounds/train.wav")
        await asyncio.sleep(9)
        await control_multiple_relays({"spots": devices["spots"]}, "off")

    elif gift_value == 1000:
        await control_multiple_relays({"spots": devices["spots"]}, "on")
        controller.send_command(PINGPONG_MACHINE_URL)
        controller.send_command(SMOKE_MACHINE_URL)
        controller.send_command(SMOKE_TWO_MACHINE_URL)
        play_video_web('./videos/thriller.mp4')
        play_sound_web(f"./sounds/thriller.wav")
        await asyncio.sleep(14)
        controller.send_command(PINGPONG_MACHINE_URL)
        await control_multiple_relays({"spots": devices["spots"]}, "off")

    elif gift_value == 1500:
        await control_multiple_relays({"spots": devices["spots"], "neige": devices["neige"]}, "on")
        play_video_web('./videos/film_300.mp4')
        play_sound_web(f"./sounds/jump.wav")
        await asyncio.sleep(20)
        await control_multiple_relays({"neige": devices["neige"], "spots": devices["spots"]}, "off")

    elif gift_value == 1999:
        await control_multiple_relays(
            {"spots": devices["spots"], "bulles": devices["bulles"], "neige": devices["neige"]}, "on")
        play_video_web('./videos/reine-des-neiges.mp4')
        await asyncio.sleep(30)
        await control_multiple_relays(
            {"neige": devices["neige"], "bulles": devices["bulles"], "spots": devices["spots"]}, "off")
        controller.send_command(SMOKE_MACHINE_URL)
        controller.send_command(SMOKE_TWO_MACHINE_URL)

    elif gift_value == 3000:
        await control_multiple_relays(
            {"spots": devices["spots"], "bulles": devices["bulles"], "neige": devices["neige"],
             "mousse": devices["mousse"]}, "on")
        play_video_web('./videos/guiles.mp4')
        play_sound_web(f"./sounds/guiles.wav")
        await asyncio.sleep(20)
        await control_multiple_relays(
            {"mousse": devices["mousse"], "neige": devices["neige"], "bulles": devices["bulles"],
             "spots": devices["spots"]}, "off")
        controller.send_command(SMOKE_MACHINE_URL)
        controller.send_command(SMOKE_TWO_MACHINE_URL)

    elif gift_value == 4000:
        await control_multiple_relays(
            {"spots": devices["spots"], "bulles": devices["bulles"], "neige": devices["neige"],
             "mousse": devices["mousse"]}, "on")
        controller.send_command(PINGPONG_MACHINE_URL)
        play_video_web('./videos/turn-down-to-what.mp4')
        await asyncio.sleep(22)
        controller.send_command(SMOKE_MACHINE_URL)
        controller.send_command(SMOKE_TWO_MACHINE_URL)
        await asyncio.sleep(2)
        controller.send_command(SMOKE_MACHINE_URL)
        controller.send_command(SMOKE_TWO_MACHINE_URL)
        controller.send_command(PINGPONG_MACHINE_URL)
        await control_multiple_relays(
            {"mousse": devices["mousse"], "neige": devices["neige"], "bulles": devices["bulles"],
             "spots": devices["spots"]}, "off")

    elif gift_value == 5000:
        await control_multiple_relays(
            {"spots": devices["spots"], "bulles": devices["bulles"], "neige": devices["neige"],
             "mousse": devices["mousse"]}, "on")
        controller.send_command(PINGPONG_MACHINE_URL)
        play_video_web('./videos/interstellar.mp4')
        play_sound_web(f"./sounds/interstellar.wav")
        await asyncio.sleep(30)
        controller.send_command(SMOKE_MACHINE_URL)
        controller.send_command(SMOKE_TWO_MACHINE_URL)
        await asyncio.sleep(2)
        controller.send_command(SMOKE_MACHINE_URL)
        controller.send_command(SMOKE_TWO_MACHINE_URL)
        controller.send_command(PINGPONG_MACHINE_URL)
        await control_multiple_relays(
            {"mousse": devices["mousse"], "neige": devices["neige"], "bulles": devices["bulles"],
             "spots": devices["spots"]}, "off")