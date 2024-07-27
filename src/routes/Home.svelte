<script>
  import LanguageSelect from "$lib/LanguageSelect.svelte";
  import ThemeSelect from "$lib/ThemeSelect.svelte";
  import { isDarkTheme } from "$stores/AppStore";
  import { t as translation } from "../locale/i18n";
</script>

<nav class="h-8 {$isDarkTheme ? 'bg-[#282727]' : 'bg-slate-100'}   flex flex-row-reverse pr-4">
  <LanguageSelect />
  <ThemeSelect />
</nav>

<h1 class="p-5 m-5 {$isDarkTheme ? 'bg-black text-white' : 'bg-slate-200 text-black'} rounded-md">
  {@html $translation("greeting")} <br />
  <p class="text-xs">{@html $translation("message")}</p>
  <br />
</h1>
