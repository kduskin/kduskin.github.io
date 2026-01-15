---
layout: default
---

## About Me

I am a PhD candidate at the <a href="https://www.washington.edu">University of Washington</a> where I conduct research with the <a href="https://ischool.uw.edu/research/center-informed-public"> Center for an Informed Public</a>. I am advised by <a href="https://ischool.uw.edu/people/faculty/profile/jevinw">Jevin West</a> and <a href="https://ischool.uw.edu/people/faculty/profile/espiro">Emma Spiro</a> and supported through the National Science Foundation as an <a href="https://www.nsfgrfp.org/about.html"> NSF Graduate Research Fellow</a>. <br/><br/>

My research encompasses topics across computational social science, primarily focusing on online political discourse, the role of algorithmic recommenders, and issues of misinformation and polarization. My dissertation focuses on the relationship between deployed algorithmic systems and problematic online information environments. I leverage data science, network science, and machine learning to better understand the social environment in which algorithm systems operate and how we might design future algorithmic systems with prosocial outcomes in mind.

<br/><br/>

## Recent News <a href="/news" class="link-button">View all</a>

<div class="news-list">
    {% for item in site.data.news limit:3 %}
        <div class="news-item">
            <div class="news-date">{{ item.date | date: "%Y-%m-%d" }}</div>
            <div class="news-content">{{ item.content | markdownify }}</div>
        </div>
    {% endfor %}
</div>

## Recent Research <a href="/research" class="link-button">View all</a>

{% for pub in site.data.publications limit:2 %}
<div class="publication">
    <div class="pub-thumbnail">
        <a href="/papers/{{ pub.title | slugify }}">
            <img src="{{ pub.thumbnail }}" alt="Thumbnail for {{ pub.title }}">
        </a>
    </div>
    <div class="pub-content">
        <h3>{{ pub.title }}</h3>
        <p class="authors">
            {% for author in pub.authors %}
                {%- if forloop.last %} and {% endif %}
                {%- if author == "Soham De" -%}
                    <strong>{{ author }}</strong>
                {%- else -%}
                    {{ author }}
                {%- endif -%}
                {%- unless forloop.last %}, {% endunless %}
            {%- endfor %}
            {%- if pub.equal_contribution %} ‡{% endif %}
        </p>
        <p class="venue"><em>{{ pub.venue }}. {{ pub.year }}</em></p>
        <div class="pub-links">
            {% if pub.links.abstract %}<a href="{{ pub.links.abstract }}">Abstract</a>{% endif %}
            {% if pub.links.paper %}<a href="{{ pub.links.paper }}">PDF</a>{% endif %}
            {% if pub.links.code %}<a href="{{ pub.links.code }}">Code</a>{% endif %}
            <a class="bibtex-btn" data-bibtex="{{ pub.bibtex | default: 'No BibTeX available' }}">
                <svg class="copy-icon" viewBox="0 0 16 16" fill="currentColor">
                    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"/>
                    <path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"/>
                </svg>
                Copy BibTeX
            </a>
        </div>
    </div>
</div>
{% endfor %}

<!-- ## Teaching & Service <a href="/teaching" class="link-button">View all</a>

I serve as a reviewer and/or PC member for CHI, CSCW, WWW, ICWSM, CACM and IC2S2. I co-organise the <a href="https://joyojeet.people.si.umich.edu/influencers.htm">Social Media and Society in India conference</a> annually, where I also chair the student session. I'm a teaching assistant for <a href="https://www.washington.edu/students/crscat/imt.html#imt573">IMT 573: Data Science I</a> taught by <a href="https://faculty.washington.edu/msaveski">Martin Saveski</a> (usually, every Autumn quarter). <a href="https://ameliadogan.github.io/">Amelia</a> and I are the Social Co-Chairs for the Doctoral Students' Association at the iSchool.<br/><br/>

Website design was inspired by <a href="https://faculty.washington.edu/msaveski">Martin Saveski</a>, <a href="https://debarghyadas.com/">Deedy Das</a> and <a href="https://vis.csail.mit.edu/">The MIT Visualization Group</a>. Feel free to fork it! -->


