---
layout: default
title: Books
---

<div class="book-grid">

<div class="book" onclick="toggleBook(this)">
<img src="/assets/images/books/tomorrow_x3.jpg">
<div class="book-title">Tomorrow, and Tomorrow, and Tomorrow</div>
</div>

<div class="book" onclick="toggleBook(this)">
<img src="/assets/images/books/hock_chye.jpg">
<div class="book-title">Hock Chye</div>
</div>

<div class="book" onclick="toggleBook(this)">
<img src="/assets/images/books/sophies_wrold.jpg">
<div class="book-title">Sophie's World</div>
</div>

</div>

<div class="book-notes" id="note-0" style="display:none;">
<b>Tomorrow, and Tomorrow, and Tomorrow</b>
<p>Different book, a view into the world of gamers.</p>
</div>

<div class="book-notes" id="note-1" style="display:none;">
<b>Hock Chye</b>
<p>About Singapore's greatest ever comic.</p>
</div>

<div class="book-notes" id="note-2" style="display:none;">
<b>Sophie's World</b>
<p>Sophie's world is an exploration of the great phiolophical concepts of Western thought. The book begins with a quote from Goethe, "He who cannot draw on three thousand years is living from hand to mouth".</p>
<p>The two philosopher's that stood out the most for me were Baruch Spinoza and Jean-Paul Sartre. Spinoza was a part of the rationalistic tradition which believed that human life is subject to the universal laws of nature. Spinoza was a monist, he did not have a dualistic view of reality. Spinoza believed that all material things and all thoughts are an expression of nature, everything is One. He believed that laws of nature to be the ineer cause of everything that happens. Spinoza had a deterministic view of the world. Humans are as determined by inner potential and outer opportunities as a tree in a garden. A tree with better conditions for growing will grow better, but an apple tree with not have the ability to bear pears or plums. Spinoza's recommendation for happiness was to see everything from the perspective of eternity.</p>
<p>Jean-Paul Sartre's existentialism became popular in the 1940s, after WW II. His existentialism was an athiestic existentialism. According to Sartre, humans have no innate nature and thus create it themselves. It is therefore useless to search for the meaning of life in general. He saw us actors dragged on to the stage, we must improvise and decide how to live ourselves. Sartre says that man feels aline in a world without meaning and feels angst. However, he was not a nihilist. Sartre believed that it is we ourseleves who must create meaning in our lives, to exist is to create your own life. Two people can be present in the same room and yet experience it quite differently, because we contribute our own meaning. We annihilate whatever is irrelevant for us. If you plan to meet someone at a cafe, you 'see' their absence. If you are waiting for call, you 'hear' them not calling. Another thing that this book pointed out was how influential the theories of Darwin and Freud been to philosophy.</p>
</div>

<script>
function toggleBook(el) {
  var books = document.querySelectorAll('.book');
  var index = Array.prototype.indexOf.call(books, el);
  var notes = document.querySelectorAll('.book-notes');
  var note = document.getElementById('note-' + index);
  var wasOpen = note.style.display === 'block';

  for (var i = 0; i < notes.length; i++) notes[i].style.display = 'none';
  for (var i = 0; i < books.length; i++) books[i].classList.remove('active');

  if (!wasOpen) {
    note.style.display = 'block';
    el.classList.add('active');
    note.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
  }
}
</script>
