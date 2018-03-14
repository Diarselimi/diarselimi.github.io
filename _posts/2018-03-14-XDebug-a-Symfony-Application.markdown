---
title:  "XDebug a Symfony Application with PHPStorm"
date:   2018-03-14 13:15:00
description: Here are the steps to setup the xdebug and Debug a controller with PHPStorm.
---

<h1 id="xdebug-a-symfony-application-with-phpstorm">XDebug a Symfony Application with PHPStorm</h1>
<blockquote>
<p>Here are the steps to setup the xdebug and Debug a controller with PHPStorm</p>
</blockquote>
<h6 id="info-all-the-commands-here-are-for-mac-and-linux-systems.">Info: All the commands here are for Mac and Linux systems.</h6>
<p>This is for all the PHP developers who are tired of <code>var_dump()</code>, <code>print_r()</code>, <code>dump()</code>.</p>
<h2 id="setup-the-xdebug">Setup the XDebug</h2>
<blockquote>
<p>Note: If you have xdebugger already installed skip to the <strong>Let’s debug a Controller</strong></p>
</blockquote>
<p>Go to this url and follow the steps to get apropriate xdebug for your system.<br>
<a href="https://xdebug.org/wizard.php">https://xdebug.org/wizard.php</a></p>
<blockquote>
<p>Note: For bash users execute this command to get the <code>phpinfo()</code> for the wizard <code>php -i &gt; ~/Desktop/phpinfo.txt</code> than copy the content and paste it to the wizard website and follow the steps.</p>
</blockquote>
<p>This is my <code>php.ini</code> configuration for <strong>xdebug</strong> to find your <code>php.ini</code> type the following command <code>php -i | grep "php.ini"</code> and you will se the path to the <code>php.ini</code> file.</p>
<pre><code>[xdebug]
zend_extension="~path-to-your-php-libraries/xdebug.so" #Get this from wizard.php
xdebug.remote_enable = 1
xdebug.remote_autostart = 1
xdebug.remote_port="9000"
xdebug.profiler_enable=1
</code></pre>
<p>For the configurations to take place just execute <code># apache2ctl restart</code> or restart Xampp or whichever engine you are using.<br>
<a href="https://www.cyberciti.biz/faq/unix-linux-restart-php-service-command/">Click here if the command is not working for you</a></p>
<p>Next go to PHPStorm preferences, then navigate under Languages &amp; Frameworks &gt; PHP<br>
You should see this window</p>
<p><img src="https://lh3.googleusercontent.com/qOalHkQIcJ2qmocpV-TZgafK4LXouAMMQPx7HeyCLzTV8b55MYDBMVfeYKr8KM3Bs3INHZFgsqT-9A" alt=""><br>
After you click the <strong>…</strong> button in the preferences window you should se another window <strong>CLI Interpreters</strong> and inside this windows under PHP Exeutable you should se Debugger: Xdebug… if it’s correctly enabled.</p>
<h2 id="lets-debug-a-controller">Let’s debug a Controller</h2>
<h6 id="asddasdadasdasdasd">asddasdadasdasdasd</h6>
<p>Open one Controller and</p>

