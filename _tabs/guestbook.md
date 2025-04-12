---
layout: page
title: GUEST
icon: fas fa-comments
<<<<<<< Updated upstream
permalink: /guestbook/
=======
permalink: /comments/
>>>>>>> Stashed changes
comments: true
order: 5
---

방명록 ✨

> 주의사항 :
> - 글이 올라가는 데 시간이 오래 걸릴 수 있습니다


<<<<<<< Updated upstream
<form method="POST" action="https://comment-w-guestbook.lanitoous.workers.dev/api/handle/form" class="comment-form">
  <input type="text" name="fields[name]" placeholder="닉네임" required>
  <textarea name="fields[message]" placeholder="메시지를 입력하세요" required></textarea>
  <input type="hidden" name="options[slug]" value="2025">
  <button type="submit">방명록 남기기</button>
</form>

<div class="comments-container">
  {% assign comment_files = site.data.comments %}
  {% for file in comment_files %}
    {% assign entry = file[1] %}
    <div class="comment-bubble">
      <div class="name">{{ entry.name }}</div>
      <div class="message">{{ entry.message }}</div>
      <div class="date">{{ entry.date | date: "%Y년 %-m월 %-d일 %H시 %M분" }}</div>
    </div>
  {% endfor %}
</div>

<style>
.comment-form {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  margin-top: 1.5rem;
}

.comment-form input[type="text"],
.comment-form textarea {
  padding: 0.5rem;
  border: 1px solid #ccc;
  border-radius: 0.5rem;
  background-color: var(--main-bg);
  color: var(--text-color);
}

.comment-form textarea {
  resize: vertical;
  height: 100px;
}

.comment-form button {
  align-self: flex-end;
  padding: 0.4rem 1rem;
  background-color: #007acc;
  color: white;
  border: none;
  border-radius: 0.5rem;
  cursor: pointer;
}

.comments-container {
  margin-top: 2rem;
  display: flex;
  flex-direction: column;
  gap: 1.2rem;
=======

<!-- guestbook.md -->
<div style="margin-bottom: 1em;">
  <form method="POST" action="https://comment-w-guestbook.lanitoous.workers.dev/api/handle/form" style="display: flex; flex-direction: column; gap: 0.5em; max-width: 400px;">
    <input type="text" name="name" placeholder="Name" required style="padding: 0.5em; border: 1px solid #ccc; border-radius: 8px;">
    <textarea name="message" placeholder="Your Comment" required rows="3" style="padding: 0.5em; border: 1px solid #ccc; border-radius: 8px;"></textarea>
    <button type="submit" style="padding: 0.5em; background: #333; color: #fff; border: none; border-radius: 8px;">남기기</button>
  </form>
</div>

---

***
<br/>

<!---댓글란--->


{% assign all_comments = site.data.comments %}
{% for filename in all_comments %}
  {% assign comment = filename[1] %}
  <div class="comment-bubble">
    <strong>{{ comment.name }}</strong>
    <div class="comment-date">
      {{ comment.date | date: "%Y년 %m월 %d일 %H:%M" }}
    </div>
    <div class="comment-message">{{ comment.message }}</div>
  </div>
{% endfor %}



<style>
.comment-list {
  display: flex;
  flex-direction: column;
  gap: 1em;
  margin-top: 1.5em;
>>>>>>> Stashed changes
}

.comment-bubble {
  position: relative;
<<<<<<< Updated upstream
  max-width: 100%;
  padding: 1rem;
  background: var(--card-bg);
  border-radius: 1rem;
  color: var(--text-color);
  box-shadow: 0 2px 5px rgba(0,0,0,0.15);
}

.comment-bubble .name {
  font-weight: bold;
  margin-bottom: 0.3rem;
}

.comment-bubble .date {
  font-size: 0.8rem;
  color: #888;
  margin-top: 0.5rem;
}

html[data-theme="dark"] .comment-form input,
html[data-theme="dark"] .comment-form textarea {
  background-color: #222;
  border-color: #444;
  color: #eee;
}

html[data-theme="dark"] .comment-form button {
  background-color: #3399ff;
}

html[data-theme="dark"] .comment-bubble {
  background-color: #333;
  color: #eee;
}

html[data-theme="dark"] .comment-bubble::after {
  border-color: #333 transparent transparent transparent;
}
</style>
=======
  max-width: 90%;
  padding: 1em;
  border-radius: 1em;
  background-color: var(--bubble-bg, #f1f1f1);
  color: var(--text-color, #333);
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.05);
}

.comment-bubble::after {
  content: "";
  position: absolute;
  left: 1em;
  bottom: -10px;
  width: 0;
  height: 0;
  border: 10px solid transparent;
  border-top-color: var(--bubble-bg, #f1f1f1);
}

.comment-header {
  display: flex;
  justify-content: space-between;
  margin-bottom: 0.5em;
  font-size: 0.9em;
  color: #666;
}

.comment-name {
  font-weight: bold;
}

.comment-message {
  white-space: pre-wrap;
}

.comment-bubble {
  background-color: var(--card-bg, #f4f4f4);
  color:  var(--text-color, #000);
  padding: 1em;
  margin: 1em 0;
  border-radius: 15px;
  max-width: 500px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.05);
  transition: background-color 0.3s ease, color 0.3s ease;


  .comment-date {
    font-size: 0.85em;
    color: #555;
    margin-top: 0.25em;
  }

  .comment-message {
    margin-top: 0.5em;
    white-space: pre-wrap;
  }
}


}

</style>
>>>>>>> Stashed changes
