<template>
  <div class="bg-background text-primary font-sans">
    <div class="container mx-auto">

      <header class="flex bg-background/50 backdrop-blur-lg sticky top-0 items-center justify-between border-b-2">
        <div class="p-4 font-bold text-2xl">Kutaev</div>
        <nav class="space-x-8 p-2 text-primary">
          <a href="#" class="hover:text-blue-500 duration-300 p-2">Home</a>
          <a href="#episodes" class="hover:text-blue-500 duration-300 p-2">Episodes</a>
          <a href="#about" class="hover:text-blue-500 duration-300 p-2">About</a>
          <a href="#contact" class="hover:text-blue-500 duration-300 p-2">Contact</a>
        </nav>
      <Button class="flex space-x-4 items-center">
        <Icon name="mdi:login" />
        <p>Auth</p>
      </Button>
      </header>



      <Alert class="mt-2">
        <AlertTitle>Alert!</AlertTitle>
        <AlertDescription>
          Call alert from base.
        </AlertDescription>
      </Alert>
      <AlertForm class=""/>


      <!-- Podcast Section -->
      <div class="flex items-center justify-center w-auto p-8 space-x-8">
        <!-- Podcast Image -->
        <img src="/images/img.png" alt="Podcast Image" class="w-[650px] rounded-lg">
        <!-- Podcast Description -->
        <div class="max-w-[650px]">
          <h1 class="text-5xl font-bold leading-tight">Take your podcast to the</h1>
          <h2 class="text-6xl font-bold italic leading-tight">Next Level</h2>
          <p class="text-lg mt-6">Listen on</p>
          <div class="flex space-x-4 mt-2">
            <a href="#" class="podcast-link"><Icon name="ph:meta-logo" size="3rem"/></a>
            <a href="#" class="podcast-link"><Icon name="ph:soundcloud-logo" size="3rem"/></a>
            <a href="#" class="podcast-link"><Icon name="ph:spotify-logo" size="3rem"/></a>
            <a href="#" class="podcast-link"><Icon name="ph:apple-logo" size="3rem"/></a>
            <a href="#" class="podcast-link"><Icon name="ph:x-logo" size="3rem"/></a>
          </div>

        </div>

      </div>

      <!-- Latest Episodes Section -->
      <div class="p-8" id="episodes">
        <div class="flex items-center justify-between">
          <h1 class="text-6xl font-bold">Latest Release</h1>
          <AlertDialog>
            <AlertDialogTrigger class="p-2">View all release</AlertDialogTrigger>
            <AlertDialogContent>
              <AlertDialogHeader>
                <AlertDialogTitle>Are you absolutely sure?</AlertDialogTitle>
                <AlertDialogDescription>
                  This action cannot be undone. This will permanently delete your account
                  and remove your data from our servers. :) (no)
                </AlertDialogDescription>
              </AlertDialogHeader>
              <AlertDialogFooter>
                <AlertDialogCancel>Cancel</AlertDialogCancel>
                <AlertDialogAction>Continue</AlertDialogAction>
              </AlertDialogFooter>
            </AlertDialogContent>
          </AlertDialog>

        </div>
        <!-- Episode Cards -->
        <action-form-episode-card
          title="Mic tricks to take you to the next level"
          category="Tips & Tricks"
          episodeNumber="Episode 3"
          description="Stop rolling with those default settings on your mic. These small tweaks will take you from sounding good to great."
          image="/images/post_1.png"
      />
        <action-form-episode-card
          title="Should you get outboard audio gear?"
          category="Gear"
          episodeNumber="Episode 2"
          description="Is hardware really worth it when it comes to podcasting? The answer is... it depends. Here’s our reasons on why you might want to consider picking something up."
          image="/images/post_2.png"
      />
        <action-form-episode-card
            title="The best microphone under $200"
            category="Gear"
            episodeNumber="Episode 1"
            description="With so many microphones on the market, how are you supposed to know what’s the best? Take a look at our top picks."
            image="/images/post_3.png"
        />
      </div>

      <!-- Jacob Paulaner Section -->
      <div id="about" class="flex items-center justify-center w-auto p-8 space-x-8">
        <div class="max-w-[650px]">
          <h1 class="text-5xl pb-4 font-semibold leading-tight">Jacob Paulaner</h1>
          <h2 class="text-xl pb-4 font-thin leading-tight">Jacob has a background in audio engineering and has been podcasting since the early days. He’s here to help you level up your game by sharing everything he’s learned along the way.</h2>
          <h2 class="text-lg mt-6 font-bold">Social media</h2>
          <div class="flex space-x-4 mt-2">
            <a href="#" class="podcast-link"><Icon name="ph:x-logo" size="3rem"/></a>
            <a href="#" class="podcast-link"><Icon name="ph:facebook-logo" size="3rem"/></a>
            <a href="#" class="podcast-link"><Icon name="ph:twitch-logo" size="3rem"/></a>
            <a href="#" class="podcast-link"><Icon name="ph:youtube-logo" size="3rem"/></a>
          </div>
        </div>
        <img src="/images/Jacob.png" alt="Jacob Paulaner" class="w-[650px] rounded-lg">
      </div>

      <!-- Subscription Form -->
      <div id="contact" class="flex items-center justify-evenly gap-2">
        <SubscriptionForm title="Email Newsletter" description="Subscribe for updates" />
      </div>

      <!-- Review Cards Section -->
      <div class="pt-16 pb-16 flex flex-wrap  justify-center   gap-10">
        <ReviewCard name="Betty Lacey" comment="I can’t recommend this podcast enough" :rating=2 />
        <ReviewCard name="Adam Driver" comment="Jacob is the best in the business" :rating=5 />
        <ReviewCard name="Marcus Brown" comment="A wealth of audio knowledge" :rating=1 />
        <ReviewCard name="Marcus Brown" comment="A wealth of audio knowledge" :rating=1 />
        <ReviewCard name="Jessica Knowl" comment="Every episode is a gem!" :rating=3 />
        <ReviewCard name="Scott Adams" comment="Whoa whoa, let me take some notes!" :rating=5 />
        <ReviewCard name="Steven Blast" comment="I’ve upped my game considerably since I started listening" :rating=4 />
        <ReviewCard name="Steven Blast" comment="I’ve upped my game considerably since I started listening" :rating=4 />
      </div>
      <div class="flex justify-center gap-20 border-t-2 pb-10 pt-10">
        <div class="">
          <h1 class="text-4xl pb-4">Cataway</h1>
          <div>
            <a href="#" class="podcast-link"><Icon name="ph:meta-logo" size="1.4rem"/></a>
            <a href="#" class="podcast-link"><Icon name="ph:soundcloud-logo" size="1.4rem"/></a>
            <a href="#" class="podcast-link"><Icon name="ph:spotify-logo" size="1.4rem"/></a>
          </div>
        </div>
        <div class="flex flex-col ">
          <a class="p-1" href="#">Home</a>
          <a class="p-1" href="#">About</a>
          <a class="p-1" href="#">Episodes</a>
          <a class="p-1" href="#">Contact</a>
        </div>
        <div class="flex flex-col ">
          <a class="p-1" href="#">Style Guide</a>
          <a class="p-1" href="#">Instructions</a>
          <a class="p-1" href="#">Changelog</a>
          <a class="p-1" href="#">Credit</a>
          <a class="p-1" href="#">Powered by Webflow</a>
          <a class="p-1" href="#">Licenses</a>
        </div>
        <div class="flex space-x-4 mt-2">
          <a href="#" class="podcast-link"><Icon name="ph:meta-logo" size="2rem"/></a>
          <a href="#" class="podcast-link"><Icon name="ph:soundcloud-logo" size="2rem"/></a>
          <a href="#" class="podcast-link"><Icon name="ph:spotify-logo" size="2rem"/></a>
          <a href="#" class="podcast-link"><Icon name="ph:apple-logo" size="2rem"/></a>
          <a href="#" class="podcast-link"><Icon name="ph:x-logo" size="2rem"/></a>
        </div>
      </div>
    </div>


  </div>
</template>

<style scoped>
/* Add scoped styles here */
.podcast-link {
  padding: 0.5rem;
  transition: transform 0.3s;
}

.podcast-link:hover {
  transform: translateY(-3px);
  filter: drop-shadow(1px 1px 2px);
}
</style>

<script setup lang="ts">
import SubscriptionForm from "~/components/Action/Form/SubscriptionForm.vue";
import ReviewCard from "~/components/Action/Form/reviewCard.vue";
import AlertForm from "~/components/Action/Form/AlertForm.vue";
import {AlertDialog} from "~/components/ui/alert-dialog";



</script>
