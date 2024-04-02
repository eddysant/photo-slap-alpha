<script lang="ts">
  import { invoke } from "@tauri-apps/api/tauri"

  let timer = "";
  let greetMsg = ""

  async function greet(){
    // Learn more about Tauri commands at https://tauri.app/v1/guides/features/command
    greetMsg = await invoke("greet", { timer })
  }
</script>

<div>
  <form class="row" on:submit|preventDefault={greet}>
    <input id="auto-shuffle" type="checkbox" /> auto shuffle
    <input id="include-video" type="checkbox" /> include video
    <input id="use-transitions" type="checkbox" /> use transitions
    <input id="black-background" type="checkbox" /> black background
    <input id="slideshow-timer" type="number" bind:value={timer} /> slideshow timer
    <button type="submit">Save & Close</button>
  </form>
</div>