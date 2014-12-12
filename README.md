activeQueue
===========

an example of extending Javascript queues by Stephen Morley

http://code.stephenmorley.org/javascript/queues/

My live example can be viewed at:

http://munibox.altervista.org/examples/activeQueue/

NOTE: This sub-domain will move in the near future.

I had a task. Create a visual for phone calling queue.
When I Googled: ''javascript queue'' that link was first.
I usually don't take the first link, but for some reason
I clicked it. I was pleasently surprised to find 
simple, minimul code - just what I was looking for.

After a few hours of playing with I thought I understood
it. I realized I did not when side effects appeared.

My original extension was:

<code>
  /* Returns any valid item on the queue - given the index.
  */
  this.look = function(n){
    return ((n >= 0 && n <= queue.length) ? queue[n] : undefined);
  }
</code>

The Correct extension is:

<tty>
  /* Returns any valid item on the queue - given the index.
  */
  this.look = function(n){
    return ((n >= 0 && n <= queue.length) ? queue[n + offset] : undefined);
  }
</tty>

The extension allows one to look and modify and item in the queue.



