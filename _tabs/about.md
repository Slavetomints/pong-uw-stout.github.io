---
layout: default
permalink: /about/
order: 1
---

<div>
    <div class="about_page_text_container">
        <h1>About Us</h1>
        <p>PONG is cool. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
            labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum
            dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia
            deserunt mollit anim id est laborum.</p>
    </div>
</div>

<div class="dark_bg">
   <div class="exec_content_container">
        <h1>Execs</h1>
        <div class="flex exec_container">
            {% for exec in site.data.execs %}
                <div class="flex exec_capsule">
                    <img src="{{ exec.photo }}" alt="photo of {{exec.name}}">
                    <div class="block">
                        <div class="exec_capsule_header">
                            <div class="exec_capsule_header_text_container">
                                <div class="exec_capsule_name">{{exec.name}}</div>
                                <div class="exec_capsule_role">{{exec.role}}</div>
                            </div>
                        </div>
                        <div class="flex exec_capsule_link_container">
                            {% for social in exec.socials %}
                            <a href="{{ social.url }}" class="exec_capsule_link" target="_blank" rel="noopener"  style="background-color: {{site.data.socials[social.type].color}};">
                                <i class="fa-brands fa-{{ site.data.socials[social.type].icon}}"></i>
                            </a>
                            {% endfor %}   
                        </div>
                    </div>
                </div>
            {% endfor %}
        </div>
    </div>
</div>