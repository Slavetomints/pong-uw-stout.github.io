---
layout: default
permalink: /about/
order: 1
---

<div>
    <div class="about_page_text_container">
        <h1>About Us</h1>
        <p>Meet our execs and staff members!</p>
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
                                <i class="{{ site.data.socials[social.type].icon}}"></i>
                            </a>
                            {% endfor %}   
                        </div>
                    </div>
                </div>
            {% endfor %}
        </div>
    </div>
</div>
<br>

<div class="dark_bg">
   <div class="exec_content_container">
        <h1>Staff</h1>
        <div class="flex exec_container">
            {% for staff in site.data.staff %}
                <div class="flex exec_capsule">
                    <img src="{{ staff.photo }}" alt="photo of {{staff.name}}">
                    <div class="block">
                        <div class="exec_capsule_header">
                            <div class="exec_capsule_header_text_container">
                                <div class="exec_capsule_name">{{staff.name}}</div>
                                <div class="exec_capsule_role">{{staff.role}}</div>
                            </div>
                        </div>
                        <div class="flex exec_capsule_link_container">
                            {% for social in staff.socials %}
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
<<<<<<< Updated upstream
=======
</div>
<br>


<div class="dark_bg">
   <div class="content_container">
        <h1>Advisors</h1>
        <div class="flex container">
            {% for advisor in site.data.advisors %}
                <div class="flex capsule">
                    <img src="{{ advisor.photo }}" alt="photo of {{advisor.name}}">
                    <div class="block">
                        <div class="capsule_header advisor">
                            <div class="capsule_header_text_container">
                                <div class="capsule_name">{{advisor.name}}</div>
                                <div class="capsule_role">{{advisor.role}}</div>
                            </div>
                        </div>
                        <div class="flex capsule_link_container">
                            {% for social in advisor.socials %}
                                {% assign href = social.url %}
                                {% if social.type == "email" %}
                                    {% assign href = "mailto:" | append: social.url %}
                                {% endif %}
                                <a href="{{ href }}" class="capsule_link" target="_blank" rel="noopener" style="background-color: {{ site.data.socials[social.type].color }};">
                                    <i class="{{ site.data.socials[social.type].icon }}"></i>
                                </a>
                            {% endfor %}
                        </div>
                    </div>
                </div>
            {% endfor %}
        </div>
    </div>
</div>
<br>

<div class="dark_bg">
   <div class="content_container">
        <h1>Mentors</h1>
        <div class="flex container">
            {% for mentor in site.data.mentors %}
                <div class="flex capsule">
                    <img src="{{ mentor.photo }}" alt="photo of {{mentor.name}}">
                    <div class="block">
                        <div class="capsule_header mentor">
                            <div class="capsule_header_text_container">
                                <div class="capsule_name">{{mentor.name}}</div>
                                <div class="capsule_role">{{mentor.role}}</div>
                            </div>
                        </div>
                        <div class="flex capsule_link_container">
                            {% for social in mentor.socials %}
                                {% assign href = social.url %}
                                {% if social.type == "email" %}
                                    {% assign href = "mailto:" | append: social.url %}
                                {% endif %}
                                <a href="{{ href }}" class="capsule_link" target="_blank" rel="noopener" style="background-color: {{ site.data.socials[social.type].color }};">
                                    <i class="{{ site.data.socials[social.type].icon }}"></i>
                                </a>
                            {% endfor %}
                        </div>
                    </div>
                </div>
            {% endfor %}
        </div>
    </div>
</div>
<br>

<div class="dark_bg">
  <div class="content_container">
    <h1>Platinum Sponsors ($250+)</h1>
    <div class="flex container">
      {% for sponsor in site.data.pong_info.sponsors.tiers['platinum'] %}
        <div class="flex capsule">
          <img src="{{ sponsor.logo }}" alt="logo for {{ sponsor.name }}">
          <div class="block">
            <div class="capsule_header platinum">
              <div class="capsule_header_text_container">
                <div class="capsule_name">{{ sponsor.name }}</div>
                <div class="capsule_role">Platinum Sponsor</div>
              </div>
            </div>
            <div class="flex capsule_link_container">
              {% for social in sponsor.socials %}
                {% assign href = social.url %}
                {% if social.type == "email" %}
                  {% assign href = "mailto:" | append: social.url %}
                {% endif %}
                <a href="{{ href }}" class="capsule_link" target="_blank" rel="noopener" style="background-color: {{ site.data.socials[social.type].color }};">
                  <i class="{{ site.data.socials[social.type].icon }}"></i>
                </a>
              {% endfor %}
            </div>
          </div>
        </div>
      {% endfor %}
    </div>
  </div>
</div>

<div class="dark_bg">
  <div class="content_container">
    <h1>Diamond Sponsors ($100-$250)</h1>
    <div class="flex container">
      {% for sponsor in site.data.pong_info.sponsors.tiers['diamond'] %}
        <div class="flex capsule">
          <img src="{{ sponsor.logo }}" alt="logo for {{ sponsor.name }}">
          <div class="block">
            <div class="capsule_header diamond">
              <div class="capsule_header_text_container">
                <div class="capsule_name">{{ sponsor.name }}</div>
                <div class="capsule_role">Diamond Sponsor</div>
              </div>
            </div>
            <div class="flex capsule_link_container">
              {% for social in sponsor.socials %}
                {% assign href = social.url %}
                {% if social.type == "email" %}
                  {% assign href = "mailto:" | append: social.url %}
                {% endif %}
                <a href="{{ href }}" class="capsule_link" target="_blank" rel="noopener" style="background-color: {{ site.data.socials[social.type].color }};">
                  <i class="{{ site.data.socials[social.type].icon }}"></i>
                </a>
              {% endfor %}
            </div>
          </div>
        </div>
      {% endfor %}
    </div>
  </div>
</div>

<div class="dark_bg">
  <div class="content_container">
    <h1>Gold Sponsors ($0-$100)</h1>
    <div class="flex container">
      {% for sponsor in site.data.pong_info.sponsors.tiers['gold'] %}
        <div class="flex capsule">
          <img src="{{ sponsor.logo }}" alt="logo for {{ sponsor.name }}">
          <div class="block">
            <div class="capsule_header gold">
              <div class="capsule_header_text_container">
                <div class="capsule_name">{{ sponsor.name }}</div>
                <div class="capsule_role">Gold Sponsor</div>
              </div>
            </div>
            <div class="flex capsule_link_container">
              {% for social in sponsor.socials %}
                {% assign href = social.url %}
                {% if social.type == "email" %}
                  {% assign href = "mailto:" | append: social.url %}
                {% endif %}
                <a href="{{ href }}" class="capsule_link" target="_blank" rel="noopener" style="background-color: {{ site.data.socials[social.type].color }};">
                  <i class="{{ site.data.socials[social.type].icon }}"></i>
                </a>
              {% endfor %}
            </div>
          </div>
        </div>
      {% endfor %}
    </div>
  </div>
</div>


<br>
<div class="flex flex-column center">
    <h2>PONG Socials</h2>
    <p>Catch up with us on our socials!</p>
    <div class="flex capsule_link_container center dark_bg flex_wrap">
        {% for social in site.data.pong_info.socials %}
            {% assign href = social.url %}
            {% if social.type == "email" %}
                {% assign href = "mailto:" | append: social.url %}
            {% endif %}
            <a href="{{ href }}" class="capsule_link" target="_blank" rel="noopener" style="background-color: {{ site.data.socials[social.type].color }};">
                <i class="{{ site.data.socials[social.type].icon }}"></i>
            </a>
        {% endfor %}
    </div>
>>>>>>> Stashed changes
</div>