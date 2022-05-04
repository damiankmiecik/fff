<template>
  <h1>Lista towarów</h1>
  <table border="2">
    <tr>
      <th>ID towaru</th>
      <th>Produkt</th>
      <th>Rozmiar</th>
      <th>Cena</th>
      <th>Dodaj do koszyka</th>
      <th>Usuń z koszyka</th>
    </tr>
    <tr v-for="t, index in towary" :key="t.id">
      <td>{{ index + 1 }}.</td>
      <td>{{ t.name }}</td>
      <td>Rozmiar: {{ t.size }}</td>
      <td>Cena: {{ t.price }}</td>
      <td><p><button @click="t.stan++">Dodaj</button></p></td>
      <td><p><button @click="t.stan--">Usuń</button></p></td>
    </tr>
  </table>
  <h1>Koszyk</h1>
  <table border="5">
    <tr>
      <th>ID towaru</th>
      <th>Produkt</th>
      <th>Rozmiar</th>
      <th>Cena</th>
      <th>Stan</th>
    </tr>
    <tr v-for="t, index in towary" :key="t.id">
      <td>{{ index + 1 }}.</td>
      <td>{{ t.name }}</td>
      <td>Rozmiar: {{ t.size }}</td>
      <td>Cena: {{ t.price }}</td>
      <td>{{ t.stan }}</td>
    </tr>
  </table>
</template>



<script setup>
    import towary from './towary.js'
</script>

