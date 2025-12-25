---


---

<h3 id="🛡️-guild-boss-timer-•-user-guide">🛡️ Guild Boss Timer • User Guide</h3>
<p>This bot tracks the respawn times of our guild bosses across all 4 channels. Below is the manual on how to use the commands correctly.</p>
<hr>
<h3 id="️⃣-registering-a-kill-killed">1️⃣ Registering a Kill: <code>/killed</code></h3>
<p>Use this command immediately after a boss dies or if you are reporting a death that happened earlier.</p>
<p><strong>Parameters:</strong></p>
<ul>
<li>
<p><code>boss</code>: Select the boss name from the list.</p>
</li>
<li>
<p><code>channel</code>: Select the channel (1-4).</p>
</li>
<li>
<p><code>time</code>: (Optional) Leave empty for <strong>“Right Now”</strong> or enter a specific time <strong>(use Server Time)</strong>.</p>
</li>
</ul>
<p><strong>🔹 Scenario A: You just killed the boss</strong> Leave the <code>time</code> field <strong>empty</strong>.</p>
<blockquote>
<p><code>/killed boss:Anego channel:3</code></p>
</blockquote>
<p><strong>🔹 Scenario B: The boss died earlier</strong> If you forgot to register it, use the <code>time</code> field with the format <strong>HH:MM AM/PM</strong>.</p>
<ul>
<li><em>Note: You must include the space before AM/PM.</em></li>
</ul>
<blockquote>
<p><code>/killed boss:Pianus Left channel:1 time:05:30 PM</code> <code>/killed boss:Manon channel:2 time:10:15 AM</code></p>
</blockquote>
<hr>
<h3 id="️⃣-checking-status-timers">2️⃣ Checking Status: <code>/timers</code></h3>
<p>Use this command to see the full list of bosses, sorted by who spawns next.</p>
<blockquote>
<p><code>/timers</code></p>
</blockquote>
<p><strong>Understanding the Status Icons:</strong></p>
<ul>
<li>
<p>⏳ <strong>Counting Down:</strong> The boss is dead. Shows time remaining (e.g., <em>in 2 hours</em>).</p>
</li>
<li>
<p>🟢 <strong>ALIVE:</strong> The boss spawned <strong>less than 5 minutes ago</strong>. Go kill it!</p>
</li>
<li>
<p>🟠 <strong>MAYBE ALIVE:</strong> The timer hit zero <strong>more than 5 minutes ago</strong>, but no one has registered a kill yet.</p>
<ul>
<li><em>It shows how long ago it spawned (e.g., Spawned 25 minutes ago).</em></li>
</ul>
</li>
<li>
<p>❓ <strong>No Information:</strong> The timer was reset because the boss track was lost.</p>
</li>
</ul>
<hr>
<h3 id="️⃣-fixing-a-lost-timer-reset">3️⃣ Fixing a Lost Timer: <code>/reset</code></h3>
<p>Use this command <strong>ONLY</strong> when the timer is wrong.</p>
<p><strong>When to use:</strong> You check <code>/timers</code> and it says <strong>Anego is ALIVE</strong> (🟢 or 🟠) on Channel 2. You go to the map, but the boss is <strong>NOT there</strong>.</p>
<ul>
<li><em>Meaning:</em> Someone outside the guild killed it and we don’t know when.</li>
</ul>
<p><strong>Action:</strong> Use the reset command to clear the false “Alive” status.</p>
<blockquote>
<p><code>/reset boss:Anego channel:2</code></p>
</blockquote>
<p><em>This changes the status to “❓ No Information” and stops the bot from sending false alerts.</em></p>
<hr>
<h3 id="🔔-automatic-notifications">🔔 Automatic Notifications</h3>
<p>You don’t need to check the bot constantly. It will tag the channel automatically:</p>
<ol>
<li>
<p>⚠️ <strong>Warning:</strong> 15 minutes before a boss spawns.</p>
</li>
<li>
<p>⚔️ <strong>Spawn Alert:</strong> The exact moment the boss spawns.</p>
</li>
</ol>

