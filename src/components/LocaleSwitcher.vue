<template>
  <div class="locale-switcher">
    <select v-model="$i18n.locale">
      <option value="en">English</option>
      <option value="ru">Русский</option>
    </select>
  </div>
</template>
<style>
select {
  padding: 7px;
  background-color: #0f152e;
  border: var(--color) 2px solid;
  border-radius: 3px;
  color: var(--color);
}
</style>