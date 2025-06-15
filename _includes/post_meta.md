{%- assign author = site.data.authors[include.author] -%}
Posted on
<time class="dt-published" datetime="{{ include.date | date_to_xmlschema }}" itemprop="datePublished">
  {{ include.date | date: site.date_format }}
</time>
{%- if author -%}
  by <span itemprop="author" itemscope itemtype="http://schema.org/Person"><span class="p-author h-card" itemprop="name">{{ author.name }}</span></span>
{%- endif -%}