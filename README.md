activeQueue
===========

an example of extending Javascript queues by Stephen Morley

http://code.stephenmorley.org/javascript/queues/

My live example can be viewed at:

http://codesnippets.altervista.org/examples/activeQueue/

I had a task. Create a visual for phone calling queue.
When I Googled: ''javascript queue'' that link was first.
I usually don't take the first link, but for some reason
I clicked it. I was pleasently surprised to find 
simple, minimal code - just what I was looking for.

After a few hours of playing with I thought I understood
it. I realized I did not when side effects appeared.

My original extension was:

<pre>
  /* Returns any valid item on the queue - given the index.
  */
  this.look = function(n){
    return ((n &gt;= 0 && n &lt;= queue.length) ? queue[n] : undefined);
  }
</pre>

The Correct extension is:

<pre>
  /* Returns any valid item on the queue - given the index.
  */
  this.look = function(n){
    return ((n &gt;= 0 && n &lt;= queue.length) ? queue[n + offset] : undefined);
  }
</pre>

The extension allows one to look and modify items in the queue.

## Adendeum ##
* Corrections made in the queue pacing.



