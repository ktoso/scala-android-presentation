:eScala my Android
================

<div class="center bigger">
  and remove the boilerplate!
</div>

![](img/androids.png)
![](img/scala_logo.png)

---

![](img/about_me.jpg)

---
First Things First
==================

    !java
    public class MobilizationActivity extends Activity {

      Twitter twitter;

      EditText msg;
      ListView tweets;
      Button send;
      TextView hello;

      LayoutInflater inflater;

      @Override
      public void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);

        twitter = new FastTwitter();

        setContentView(R.layout.main);
        
        msg = (EditText) findViewById(R.id.msg);
        tweets = (ListView) findViewById(R.id.tweets);
        send = (Button) findViewById(R.id.send);
        hello = (TextView) findViewById(R.id.hello);

---

But let's step back...
======================

---

Collections
===========

Given a list of attendees (you),
let's

---

Guava to the rescue
===================

    !java
    List<String> girls = FluentIterable
     .from(people)
     .filter(new Predicate<Person>() {
        @Override
        public boolean apply(Person person) {
          return person != null && person.isWoman();
        }
     })
     .transform(new Function<Person, String>() {
        @Override
        public String apply(Person input) {
          return input.getFirstName() + " " + input.getLastName();
        }
     })
     .toImmutableList();

     for(String girlName : girls)
       


---

Me.sad(true)
============

![You make bunny cry](img/bunny.jpg)

---

Scala
=====
![](img/scala_logo.png)

---

Important links
===============

* [Functional Programming Principles in Scala @ Coursera](https://www.coursera.org/course/progfun) <g:plusone href="https://www.coursera.org/course/progfun"></g:plusone>
* [Scala books @ Amazon.co.uk](http://www.amazon.co.uk/s/ref=sr_nr_scat_266239_ln?rh=n%3A266239%2Ck%3Ascala&keywords=scala&ie=UTF8&qid=1348091903&scn=266239&h=700c5471dfd5e057ca5b89d7b98fe67f46ba965a)



<!-- Place this render call where appropriate -->
<script type="text/javascript">
  (function() {
    var po = document.createElement('script'); po.type = 'text/javascript'; po.async = true;
    po.src = 'https://apis.google.com/js/plusone.js';
    var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(po, s);
  })();
</script>

---

Other links
===========

* [My Guava Talk](http://www.blog.project13.pl/index.php/coding/1636/google-guava-presentation-from-google-io-extended-2012/)
* [My RoboGuice Talk](http://www.blog.project13.pl/index.php/project13/1389/conference-deep-dive-into-roboguice-cracow-mobi/)
* [Scala Words](http://ktoso.github.com/scala-words/) - a small scala library I do for fun

---

Thanks! Dziękuję! ありがとう~!
=========================
<div class="center bigger">Slides &amp;&amp; code will be blogged:</div>

.qr: 450|blog.project13.pl

<div class="center">
  <a href="http://www.project13">blog.project13.pl</a>
  || 
  <a href="http://www.twitter.com/ktosopl">@ktosopl</a>
</div>
