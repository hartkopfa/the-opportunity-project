---
title: Prize Challenge
permalink: /prize-challenge/
layout: default
class: prize

challenge-gov: https://www.challenge.gov/challenge/open-data-for-good-grand-challenge/
submission-checklist: xyz

hero:
  text: 'Win Funding to Scale Your Technology<br/>Awarding $310,000 in prizes'
  subtext: 'The [Open Data For Good Challenge](https://www.challenge.gov/challenge/open-data-for-good-grand-challenge/){: .usa-link } is now live. Awarding funding to teams who use The Opportunity Project process.'

banner-subheader:
  top:
    background: base-darkest
    line: '-light'

event-announcement:
  title:
    - Open Data
    - For Good
    - Grand Challenge
  cta: NOW LIVE
  img: 
    src: prize/top-grand-challenge-background-01.jpg  
    alt: Pointillism photo of a mountainside with evergreen trees

<!-- timeline: 
  - text: Prize Opens on Challenge.gov
    subtitle:  July 1st, 2021
    items:
      - text: General Information Session – August 23, 2:00-3:00 pm ET
        href: https://odfggcinfowebinar2.splashthat.com/
      - text: Open Data + Information Session  – September 9, 3:00-4:15 pm ET
        href: https://odfggcinfowebinartopxtoolkit.splashthat.com
  - text: Prize Submission Opens
    subtitle: September 13th, 2021
    items:
    - text: Info and Q&A – Oct 6, 5:00-6:00 pm ET
      href: http://odfggcfinalinfowebinar.splashthat.com
  - text: Prize Submission Deadline
    subtitle: October 24th, 2021
  - text: Judging Process
    subtitle: November
  - text: Winners Announced
    subtitle: December - January -->

about:
  title: How It All Started
  heading-level: 3
  left-col-width: '4'
  left-col-offset: 1
  right-col-width: '5'
  right-col-offset: 1
  skip-top-border: true
  skip-bottom-border: true
  left-col: circle-logo.md
  right:
    - body: '*In 2019, we launched The Opportunity Project Prize Challenge. The Census Bureau’s first ever prize competition, it awarded $100,000 in funding across 5 teams.*'
    - title: Why the 2019 Prize was Launched
      body: After 4 years of TOP, we created the TOP  prize challenge to help address the challenges technologists face in deploying and sustaining civic tech products.  The prize challenge aimed to support technologists in getting their solutions into the hands of communities around the country.

graphs:
  - title: User Friendly
  - title: Civic Impact
  - title: Creativity

judging:
  title: Judged by Experts
  heading-level: 3
  grid-gap-lg: true
  skip-top-border: true
  skip-bottom-border: true
  left-col: graphs-with-text.md
  right: 
    - body: Products in our first competition were scored for their creativity, user-friendliness, and potential for civic impact by panels of product, data, and policy specialists from private industry and government.

judge-photo: 
  src: prize/02_Judges_prize-winner.jpg
  alt: a man and woman handing a $20k check from The Opportunity Project to a woman on a stage
  caption: '2019 Prize Challenge winner Kristen Lewis of Measure of America receives her prize from Ron Jarmin, Acting Director of the U.S. Census Bureau and Suzette Kent, Former Federal Chief Information Officer'

past-title: Prize Challenge

winners:
  title: 2021 Winners
  # subtext: '$310k awarded in The Opportunity Project’s 2021 Open Data for Good Prize Challenge.<br/> 
  # See [challenge.gov](https://www.challenge.gov/challenge/open-data-for-good-grand-challenge/) for challenge details.'

---

{% include hero.html %}
{% include event-announcement.html data=page.event-announcement%}

{::options parse_block_html="true" /}
<section class="grid-section margin-top-6 margin-bottom-15 padding-y-3 width-full maxw-full margin-x-0">
  <div class="maxw-tablet margin-x-auto">

<!-- ### What is It?
{: .section-header }

The Open Data for Good Grand Challenge is a set of cash and in-kind prizes for teams who have created high-impact digital tools that solve problems for the public.

Please visit the official [challenge.gov posting]({{ page.challenge-gov }}) for the full rules and application requirements.

[View the rules]({{ page.challenge-gov }}){: .btn-link .btn-link__primary-red .btn-link--small .margin-top-0 .margin-left-0}
{: .margin-top-0 } -->

<!-- ### What Can You Win?
{: .section-header .margin-top-6 } -->

<!-- Prizes range from $10,000 to $50,000 with additional prizes expected to be announced!  
We're looking for tools that fit into one of these categories:
- Climate, Resilience, and the Natural Environment
- Society, Economy, and the Built Environment
- Health and COVID-19 -->

<!-- ### What Do You Have To Do?
{: .section-header .margin-top-6 }
1. Create a product using the [TOP Product Development Toolkit](/product-development/toolkit/) or in a [TOP or TOPx Sprint](/sprints) between January 1st, 2020 and October 24th, 2021
2. Attend an informational session (optional)
3. Submit your application by the deadline via email and a short submission form -->

<!-- Submissions are open from September 13, 2021 – October 24, 2021
{: .usa-alert .usa-alert--warning .usa-alert--no-icon .padding-left-2 } -->

<!-- Before you submit your application, please review the submission checklist.
[Submission Checklist (.docx) &darr;]({{ page.submission-checklist }}){: download .btn-link .btn-link__secondary-red .btn-link--small .margin-top-2 .margin-left-0 } -->

<!-- ### Timeline
{: .margin-top-6 .margin-bottom-0 }
{% include process-list.html data=page.timeline %} -->

{::options parse_block_html="false" /}
<figure>
  {% include image.html src=page.judge-photo.src alt=page.judge-photo.alt class="border-1px" %}
 <figcaption>{{ page.judge-photo.caption }}</figcaption>
</figure>

  </div>
</section>

<section class="usa-section usa-section--dark bg-base-darkest border-bottom-1px">

  <h2 class="text-center">
    {{ page.past-title }}
  </h2>

  {% include two-column-markdown.html content=page.about %}
  {% include two-column-markdown.html content=page.judging %}

  <div class="grid-section margin-bottom-6">
    <h3 class="margin-bottom-0 section-header section-header--light">{{ page.winners.title }}</h3>
    {% assign winners = site.data.products | where_exp: "item", "item.prize_status == 'Winner'" %}
    {% for winner in winners %}
      {% include prize-winner-product.html content=winner %}
    {% endfor %}
  </div>

  
</section>
