# FedCloud Catchall Operations

## Docs

Check the [README.md](https://github.com/EGI-Foundation/fedcloud-catchall-operations/blob/master/README.md) and
[FedCloud integration documentation](https://egi-federated-cloud-integration.readthedocs.io/en/latest/)


## Stable Releases

{% assign charts = site.data.index.entries.fedcloud-ops | sort: 'created' | reverse %}
<table>
  <tr>
    <th>release</th>
    <th>date</th>
  </tr>
  {% for chart in charts %}
    {% unless chart.version contains "-"%}
    <tr>
      <td>
      <a href="{{ chart.urls[0] }}">
          {{ chart.name }}-{{ chart.version | remove_first: "v" }}
      </a>
      </td>
      <td>
      <span class='date'>{{ chart.created | date_to_rfc822 }}</span>
      </td>
    </tr>
    {% endunless %}
  {% endfor %}
</table>

## Development 

<table>
  <tr>
    <th>release</th>
    <th>date</th>
  </tr>
  {% for chart in charts %}
    <tr>
      <td>
      {% unless chart.version contains "-" %}<b>{% endunless %}
      <a href="{{ chart.urls[0] }}">
          {{ chart.name }}-{{ chart.version | remove_first: "v" }}
      </a>
      {% unless chart.version contains "-" %}</b>{% endunless %}
      </td>
      <td>
      <span class='date'>{{ chart.created | date_to_rfc822 }}</span>
      </td>
    </tr>
  {% endfor %}
</table>
