<script>
    import { Heading, P, Gallery } from "flowbite-svelte";
    let images = [
        {
            alt: "Main Menu",
            src: "https://media.discordapp.net/attachments/919393991936606271/1118020469996654593/image.png",
        },
        {
            alt: "Maze Level",
            src: "https://media.discordapp.net/attachments/919393991936606271/1118020470244130857/image.png",
        },
        {
            alt: "Action Level",
            src: "https://media.discordapp.net/attachments/919393991936606271/1118020470487396464/image.png",
        },
        {
            alt: "Lesson",
            src: "https://media.discordapp.net/attachments/919393991936606271/1118020470785183774/image.png",
        },
        {
            alt: "Pause Menu",
            src: "https://media.discordapp.net/attachments/919393991936606271/1118020471045242980/image.png",
        },
        {
            alt: "End Screen",
            src: "https://media.discordapp.net/attachments/919393991936606271/1118020471284314134/image.png",
        },
    ];
    let showThumbs = false;
    let showCaptions = false;
</script>

<div class="pt-20 m-10 mx-36">
    <Heading tag="h2" class="mb-4">Timber Trek</Heading>
    <P
        weight="light"
        color="text-gray-500 dark:text-gray-400"
        class="mb-4 leading-loose"
    >
        As part of my Grade 12 Computer Science final project, I had the
        incredible opportunity to contribute to the development of Timber Trek,
        a simple yet challenging game. I worked on this project along side with
        Victor Sarca and Radin Ahari. I will be going over my contributions and
        the overall importance of our game.
    </P>

    <Heading tag="h4" weight="light" class="mb-4">UI Design</Heading>
    <P
        weight="light"
        color="text-gray-500 dark:text-gray-400"
        class="mb-4 leading-loose"
    >
        When it came to Timber Trek, creating an engaging and intuitive user
        interface was crucial. My role in this project was centered around
        designing a UI that would enhance user's interaction with the game.
        Through a careful blend of pixel art aesthetics and functionality, I
        placed buttons, menus, and graphical elements to create an immersive
        navigation experience. Along with all UI elements, I took the
        responsibilty of creating level 1, the lessons. I used a lesson class to
        help generate all lessons with the same layout, including a background,
        graphics and scrolling text.
    </P>
    <Heading tag="h4" weight="light" class="mb-4">Sound Class</Heading>
    <P
        weight="light"
        color="text-gray-500 dark:text-gray-400"
        class="mb-4 leading-loose"
    >
        In the world of gaming, audio plays a pivotal role in creating a more
        immersive experience. For Timber Trek, I took charge of implementing the
        sound class, bringing the game to life. Extensive research into sound
        libraries and technologies enabled me to integrate an array of audio
        elements that corresponded to in-game actions and events. There were
        many different options, but I chose the method using SourceDataLine,
        which loads the audio files in chunks which saves on memory and time.
    </P>
    <Heading tag="h4" weight="light" class="mb-4"
        >Importance of Learning to Survive in the Forest</Heading
    >
    <P
        weight="light"
        color="text-gray-500 dark:text-gray-400"
        class="mb-4 leading-loose"
    >
        Beyond the technical aspects of Forest Trek, we wanted to instill a
        deeper appreciation for nature and the importance of survival skills.
        Our game included many lessons to teach young teenagers on ways to
        survive in the forest. According to David Paulides of the North America
        Bigfoot Search, more than 1600 people go missing in US national
        wildlands every year. This number doesn't even account for forests that
        are not provincial and national parks, so the number could be a lot
        higher. This evidence shows a need for people to learn how to survive in
        the forest if one were to ever get lost. Hiking and going into the
        wilderness is a very common activity, so accidents while in nature can
        happen. Knowing what to do in these emergency situations like getting
        lost is crucial to survival and being rescued.
    </P>
    <Heading tag="h4" weight="light" class="mb-4"
        >Screenshots</Heading
    >
    <Gallery items={images} class="gap-4 grid-cols-2 md:grid-cols-3" />
</div>
