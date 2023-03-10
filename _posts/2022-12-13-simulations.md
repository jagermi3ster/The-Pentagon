---
keywords: fastai
title: Title
nb_path: _notebooks/2022-12-13-simulations.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-12-13-simulations.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-python"><pre><span></span><span class="p">{</span>
 <span class="s2">&quot;cells&quot;</span><span class="p">:</span> <span class="p">[</span>
  <span class="p">{</span>
   <span class="s2">&quot;attachments&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;cell_type&quot;</span><span class="p">:</span> <span class="s2">&quot;markdown&quot;</span><span class="p">,</span>
   <span class="s2">&quot;metadata&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;source&quot;</span><span class="p">:</span> <span class="p">[</span>
    <span class="s2">&quot;# 3.16 Lesson</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;&gt; Lesson about simulations and what they&#39;re used for </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- layout: default</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- toc: true</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- badges: false</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- comments: true</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- categories: [lesson]&quot;</span>
   <span class="p">]</span>
  <span class="p">},</span>
  <span class="p">{</span>
   <span class="s2">&quot;attachments&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;cell_type&quot;</span><span class="p">:</span> <span class="s2">&quot;markdown&quot;</span><span class="p">,</span>
   <span class="s2">&quot;metadata&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;source&quot;</span><span class="p">:</span> <span class="p">[</span>
    <span class="s2">&quot;# First Order of Business: Get your notebook </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- Open a terminal in vscode, run command: cd _notebooks, type &#39;wget&#39; and paste this link into said terminal and run it </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- Take notes wherever you please, but you will be graded on participating &quot;</span>
   <span class="p">]</span>
  <span class="p">},</span>
  <span class="p">{</span>
   <span class="s2">&quot;attachments&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;cell_type&quot;</span><span class="p">:</span> <span class="s2">&quot;markdown&quot;</span><span class="p">,</span>
   <span class="s2">&quot;metadata&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;source&quot;</span><span class="p">:</span> <span class="p">[</span>
    <span class="s2">&quot;# So, what is a simulation anyway? </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- A simulation is a tested scenario used for viewing results/outputs to prepare for them in real world situations </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- These can be used for games like dice rolling, spinners, etc </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- These can be used for practical things such as building structures, testing car crashes, and other things before engaging in them in the real world </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- These simulations can have the option of obeying real world physics (Gravity, collision) or they can go against these norms since this is a fictitious scenario, and couldn&#39;t happen in real life&quot;</span>
   <span class="p">]</span>
  <span class="p">},</span>
  <span class="p">{</span>
   <span class="s2">&quot;attachments&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;cell_type&quot;</span><span class="p">:</span> <span class="s2">&quot;markdown&quot;</span><span class="p">,</span>
   <span class="s2">&quot;metadata&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;source&quot;</span><span class="p">:</span> <span class="p">[</span>
    <span class="s2">&quot;# Big Question </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- Which of the following simulations could be the LEAST useful? </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- A retailer trying to identify which products sold the most </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- A restaurant determining the efficiency of robots </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- An insurance company studying the rain impact of cars </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- A sports bike company studying design changes to their new bike design </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- If you guessed a bike company, you&#39;re wrong, because the retail simulation was the right answer. Simulating robots in food service, sudying rain impact on vehicles, and new bike design can contribute a lot more to society in comparison to seeing what products sell more than others. </span><span class="se">\n</span><span class="s2">&quot;</span>
   <span class="p">]</span>
  <span class="p">},</span>
  <span class="p">{</span>
   <span class="s2">&quot;attachments&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;cell_type&quot;</span><span class="p">:</span> <span class="s2">&quot;markdown&quot;</span><span class="p">,</span>
   <span class="s2">&quot;metadata&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;source&quot;</span><span class="p">:</span> <span class="p">[</span>
    <span class="s2">&quot;# Next Big Question </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;If you were making a simulation for making a new train station, which of the following would be true about this simulation? </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- It could reveal potential problems/safety issues before construction starts </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- It cannot be used to test the train station in different weather </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- Simulation will add high costs to projects </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- Simulation is not needed because this train station already exists  </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- Potential Saftey was the right answer, because you need somewhere to test the safety and ethicness of what you&#39;re about to do before you start building it. Otherwise, let&#39;s just say you&#39;ll have a special plaque for FBI&#39;s Most Wanted</span><span class="se">\n</span><span class="s2">&quot;</span>
   <span class="p">]</span>
  <span class="p">},</span>
  <span class="p">{</span>
   <span class="s2">&quot;attachments&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;cell_type&quot;</span><span class="p">:</span> <span class="s2">&quot;markdown&quot;</span><span class="p">,</span>
   <span class="s2">&quot;metadata&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;source&quot;</span><span class="p">:</span> <span class="p">[</span>
    <span class="s2">&quot;# Simulation 1: </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Both programs below do the same thing. Given a height and a weight, they calculate how long it will take for a object to fall to the ground in a vacuum subjected to normal Earth levels of gravity. </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;However, the second one is a simulation. It calculates the distance the object has fallen every 0.1 seconds. This is useful for if you wanted a visual representation of a falling object, which pure math can&#39;t do as smoothly. &quot;</span>
   <span class="p">]</span>
  <span class="p">},</span>
  <span class="p">{</span>
   <span class="s2">&quot;cell_type&quot;</span><span class="p">:</span> <span class="s2">&quot;code&quot;</span><span class="p">,</span>
   <span class="s2">&quot;execution_count&quot;</span><span class="p">:</span> <span class="n">null</span><span class="p">,</span>
   <span class="s2">&quot;metadata&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;outputs&quot;</span><span class="p">:</span> <span class="p">[],</span>
   <span class="s2">&quot;source&quot;</span><span class="p">:</span> <span class="p">[</span>
    <span class="s2">&quot;height = float(input(</span><span class="se">\&quot;</span><span class="s2">height in meters?</span><span class="se">\&quot;</span><span class="s2">))</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;weight = input(</span><span class="se">\&quot;</span><span class="s2">weight in pounds?</span><span class="se">\&quot;</span><span class="s2">)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;stuff = (2 * (height / 9.8))**(1/2)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;print(</span><span class="se">\&quot;</span><span class="s2">It will take</span><span class="se">\&quot;</span><span class="s2">, stuff,</span><span class="se">\&quot;</span><span class="s2">seconds for an object that weighs</span><span class="se">\&quot;</span><span class="s2">,weight,</span><span class="se">\&quot;</span><span class="s2">pounds</span><span class="se">\&quot;</span><span class="s2">,</span><span class="se">\&quot;</span><span class="s2">to fall </span><span class="se">\&quot;</span><span class="s2">,height,</span><span class="se">\&quot;</span><span class="s2">meters in a vacuum</span><span class="se">\&quot;</span><span class="s2">)&quot;</span>
   <span class="p">]</span>
  <span class="p">},</span>
  <span class="p">{</span>
   <span class="s2">&quot;cell_type&quot;</span><span class="p">:</span> <span class="s2">&quot;code&quot;</span><span class="p">,</span>
   <span class="s2">&quot;execution_count&quot;</span><span class="p">:</span> <span class="n">null</span><span class="p">,</span>
   <span class="s2">&quot;metadata&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;outputs&quot;</span><span class="p">:</span> <span class="p">[],</span>
   <span class="s2">&quot;source&quot;</span><span class="p">:</span> <span class="p">[</span>
    <span class="s2">&quot;t = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;g = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;d = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;false = True</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;while false:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    t = t + 0.1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    d = 9.8 / 2 * (t**2)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if d &gt;= height:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        false = False</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    #print(d) # if you want to print the distance every time it calculates it. Too long to output to a terminal, but this could be useful to display graphically. </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    #print(t)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;print(t)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;print(d)&quot;</span>
   <span class="p">]</span>
  <span class="p">},</span>
  <span class="p">{</span>
   <span class="s2">&quot;attachments&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;cell_type&quot;</span><span class="p">:</span> <span class="s2">&quot;markdown&quot;</span><span class="p">,</span>
   <span class="s2">&quot;metadata&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;source&quot;</span><span class="p">:</span> <span class="p">[</span>
    <span class="s2">&quot;# Simulation 2: </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- This simulation is made in order to simulate movement on a 2d plane vs a 3d plane.  </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- How it works: we have multiple variables, if statements and equations under a while command in order to randomy generate steps on a 2d plane. Once it reaches the set destination, it will say that the man made it home after x amount of steps. </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- For the 3D plane, it takes a lot longer due to how big and open the 3d environment is, so there are more if statements in the 3d plane </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;(explain further)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span>
   <span class="p">]</span>
  <span class="p">},</span>
  <span class="p">{</span>
   <span class="s2">&quot;cell_type&quot;</span><span class="p">:</span> <span class="s2">&quot;code&quot;</span><span class="p">,</span>
   <span class="s2">&quot;execution_count&quot;</span><span class="p">:</span> <span class="n">null</span><span class="p">,</span>
   <span class="s2">&quot;metadata&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;outputs&quot;</span><span class="p">:</span> <span class="p">[],</span>
   <span class="s2">&quot;source&quot;</span><span class="p">:</span> <span class="p">[</span>
    <span class="s2">&quot;import random</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;x = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;y = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;nights = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;turn = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;stopped = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;turns = []</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;while (nights &lt; 100):</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    step = random.randrange(4)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if step == 0:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        x = x+1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if step == 1:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        x = x-1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if step == 2:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        y = y+1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if step == 3:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        y = y-1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    turn = turn + 1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if x == 0 and y == 0:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        nights = nights + 1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        print(</span><span class="se">\&quot;</span><span class="s2">The Man Has Made It Home After </span><span class="se">\&quot;</span><span class="s2">, turn, </span><span class="se">\&quot;</span><span class="s2">Turns</span><span class="se">\&quot;</span><span class="s2">)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        turns.append(turn)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        turn = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if turn/1000 % 1000 == 0 and x + y != 0:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        print(</span><span class="se">\&quot;</span><span class="s2">(</span><span class="se">\&quot;</span><span class="s2">, x,y, </span><span class="se">\&quot;</span><span class="s2">)</span><span class="se">\&quot;</span><span class="s2">)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if (turn &gt; 10000000):</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        stopped = stopped + 1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        turn = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        x = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        y = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        nights = nights + 1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        print(</span><span class="se">\&quot;</span><span class="s2">Caped</span><span class="se">\&quot;</span><span class="s2">)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;average = sum(turns) / len(turns)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;print(</span><span class="se">\&quot;</span><span class="s2">Avaerage</span><span class="se">\&quot;</span><span class="s2">, average, </span><span class="se">\&quot;</span><span class="s2">Ones that when&#39;t too long </span><span class="se">\&quot;</span><span class="s2">, stopped)&quot;</span>
   <span class="p">]</span>
  <span class="p">},</span>
  <span class="p">{</span>
   <span class="s2">&quot;cell_type&quot;</span><span class="p">:</span> <span class="s2">&quot;code&quot;</span><span class="p">,</span>
   <span class="s2">&quot;execution_count&quot;</span><span class="p">:</span> <span class="n">null</span><span class="p">,</span>
   <span class="s2">&quot;metadata&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;outputs&quot;</span><span class="p">:</span> <span class="p">[],</span>
   <span class="s2">&quot;source&quot;</span><span class="p">:</span> <span class="p">[</span>
    <span class="s2">&quot;import random</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;x = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;y = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;z = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;nights = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;turn = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;stopped = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;turns = []</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;while (nights &lt; 100):</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    #rando movement</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    step = random.randrange(6)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if step == 0:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        x = x+1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if step == 1:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        x = x-1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if step == 2:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        y = y+1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if step == 3:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        y = y-1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if step == 4:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        z = z+1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if step == 5:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        z = z-1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    #Turn counter</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    turn = turn + 1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    #Goal check</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if x == 0 and y == 0 and z == 0:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        nights = nights + 1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        print(</span><span class="se">\&quot;</span><span class="s2">The Bird Has Made It Home After </span><span class="se">\&quot;</span><span class="s2">, turn, </span><span class="se">\&quot;</span><span class="s2">Turns</span><span class="se">\&quot;</span><span class="s2">)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        turns.append(turn)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        turn = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if turn/1000 % 1000 == 0 and x + y + z != 0:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        print(</span><span class="se">\&quot;</span><span class="s2">(</span><span class="se">\&quot;</span><span class="s2">, x,y, </span><span class="se">\&quot;</span><span class="s2">) </span><span class="se">\&quot;</span><span class="s2">,</span><span class="se">\&quot;</span><span class="s2">| </span><span class="se">\&quot;</span><span class="s2">, z)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    #Too long Stoper</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;    if (turn &gt; 10000000):</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        stopped = stopped + 1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        turn = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        x = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        y = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        z = 0</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        nights = nights + 1</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;        print(</span><span class="se">\&quot;</span><span class="s2">Caped</span><span class="se">\&quot;</span><span class="s2">)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;average = sum(turns) / len(turns)</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;print(</span><span class="se">\&quot;</span><span class="s2">Avaerage</span><span class="se">\&quot;</span><span class="s2">, average,</span><span class="se">\&quot;</span><span class="s2">Ones that when&#39;t too long </span><span class="se">\&quot;</span><span class="s2">, stopped)&quot;</span>
   <span class="p">]</span>
  <span class="p">},</span>
  <span class="p">{</span>
   <span class="s2">&quot;attachments&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;cell_type&quot;</span><span class="p">:</span> <span class="s2">&quot;markdown&quot;</span><span class="p">,</span>
   <span class="s2">&quot;metadata&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;source&quot;</span><span class="p">:</span> <span class="p">[</span>
    <span class="s2">&quot;# Simulations in the wild</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Simulations are used extremely frequently in real life applications. One of the most common examples of simulations are video games. A games physics engine can accurately simulate objects colliding </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Another example is Blender, the software used in 3d animations class, here at Del Norte. Blender is made up of many small simulations, but one big one it uses is simulating the way light bounces off of and interacts with objects. &quot;</span>
   <span class="p">]</span>
  <span class="p">},</span>
  <span class="p">{</span>
   <span class="s2">&quot;attachments&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;cell_type&quot;</span><span class="p">:</span> <span class="s2">&quot;markdown&quot;</span><span class="p">,</span>
   <span class="s2">&quot;metadata&quot;</span><span class="p">:</span> <span class="p">{},</span>
   <span class="s2">&quot;source&quot;</span><span class="p">:</span> <span class="p">[</span>
    <span class="s2">&quot;# HW !!!</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Create a simulation. It can be anything, just has to simulate something.</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Some ideas:</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- Two objects colliding</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;- Gravity on other planets</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;AND</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="s2">&quot;Find an example of a simulation in a software/game you use, screenshot, and explain how it is a simulation&quot;</span>
   <span class="p">]</span>
  <span class="p">}</span>
 <span class="p">],</span>
 <span class="s2">&quot;metadata&quot;</span><span class="p">:</span> <span class="p">{</span>
  <span class="s2">&quot;kernelspec&quot;</span><span class="p">:</span> <span class="p">{</span>
   <span class="s2">&quot;display_name&quot;</span><span class="p">:</span> <span class="s2">&quot;Python 3&quot;</span><span class="p">,</span>
   <span class="s2">&quot;language&quot;</span><span class="p">:</span> <span class="s2">&quot;python&quot;</span><span class="p">,</span>
   <span class="s2">&quot;name&quot;</span><span class="p">:</span> <span class="s2">&quot;python3&quot;</span>
  <span class="p">},</span>
  <span class="s2">&quot;language_info&quot;</span><span class="p">:</span> <span class="p">{</span>
   <span class="s2">&quot;codemirror_mode&quot;</span><span class="p">:</span> <span class="p">{</span>
    <span class="s2">&quot;name&quot;</span><span class="p">:</span> <span class="s2">&quot;ipython&quot;</span><span class="p">,</span>
    <span class="s2">&quot;version&quot;</span><span class="p">:</span> <span class="mi">3</span>
   <span class="p">},</span>
   <span class="s2">&quot;file_extension&quot;</span><span class="p">:</span> <span class="s2">&quot;.py&quot;</span><span class="p">,</span>
   <span class="s2">&quot;mimetype&quot;</span><span class="p">:</span> <span class="s2">&quot;text/x-python&quot;</span><span class="p">,</span>
   <span class="s2">&quot;name&quot;</span><span class="p">:</span> <span class="s2">&quot;python&quot;</span><span class="p">,</span>
   <span class="s2">&quot;nbconvert_exporter&quot;</span><span class="p">:</span> <span class="s2">&quot;python&quot;</span><span class="p">,</span>
   <span class="s2">&quot;pygments_lexer&quot;</span><span class="p">:</span> <span class="s2">&quot;ipython3&quot;</span><span class="p">,</span>
   <span class="s2">&quot;version&quot;</span><span class="p">:</span> <span class="s2">&quot;3.8.10&quot;</span>
  <span class="p">},</span>
  <span class="s2">&quot;orig_nbformat&quot;</span><span class="p">:</span> <span class="mi">4</span><span class="p">,</span>
  <span class="s2">&quot;vscode&quot;</span><span class="p">:</span> <span class="p">{</span>
   <span class="s2">&quot;interpreter&quot;</span><span class="p">:</span> <span class="p">{</span>
    <span class="s2">&quot;hash&quot;</span><span class="p">:</span> <span class="s2">&quot;916dbcbb3f70747c44a77c7bcd40155683ae19c65e1c03b4aa3499c5328201f1&quot;</span>
   <span class="p">}</span>
  <span class="p">}</span>
 <span class="p">},</span>
 <span class="s2">&quot;nbformat&quot;</span><span class="p">:</span> <span class="mi">4</span><span class="p">,</span>
 <span class="s2">&quot;nbformat_minor&quot;</span><span class="p">:</span> <span class="mi">2</span>
<span class="p">}</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

</div>
 
