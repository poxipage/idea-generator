<script lang="ts">
  import { onMount } from "svelte";

  const ideas = [
    "Make a site showing your love to your best friend",
    "Make a site showing your love to your lover",
    "Make a personal page for your instagram",
    "Create a congratulation birthday page",
    "Create an invite for an event",
    "Make a site to show off your favorite hobby",
    "Create a tribute page to one of your favorite artists",
    "Create a personal start page with everything you use regularly",
    "Create an info page about an organization you are part of",
    "Create a personal page that will help you relax",
    "Create a personal page that will help you focus",
    "Create a page to keep track of your daily tasks, reminders and short/long term goals",
    "Make a page to keep track of new ideas and inspire creativity",
    "Make a page for planning a trip you want to go on",

  ]

  let idea = ""

  const getNewIdea = () => {
    idea = ideas[Math.floor(ideas.length * Math.random())]
  }
  
  onMount(() => {
		getNewIdea()
	});
</script>

<div class="w-full h-full text-base-content justify-center">
  <p> {idea} </p>
  <button class="btn mt-5" on:click={getNewIdea}>New idea</button>
</div>

<style>
</style>
