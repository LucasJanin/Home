# Merge Pi-Hole Template #

This template permet to merge mutiple pihole sensors in one.

```yml
# pi-hole
- platform: template
  sensors:
    pi_hole_dns_queries:
      friendly_name: "Pi-Hole DNS Queries Today"
      value_template: "{{ ((states('sensor.pi_hole_222_dns_queries_today') | float) + (states('sensor.pi_hole_223_dns_queries_today') | float)) | int }}"
      unit_of_measurement: "queries"
      icon_template: mdi:comment-question-outline
- platform: template
  sensors:
    pi_hole_dns_queries_cached:
      friendly_name: "Pi-Hole DNS Queries Cached Today"
      value_template: "{{ ((states('sensor.pi_hole_222_dns_queries_cached') | float) + (states('sensor.pi_hole_223_dns_queries_cached') | float)) | int }}"
      unit_of_measurement: "queries"
      icon_template: mdi:comment-question-outline      
- platform: template
  sensors:
    pi_hole_ads_blocked:
      friendly_name: "Pi-Hole Ads Blocked Today"
      value_template: "{{ ((states('sensor.pi_hole_222_ads_blocked_today') | float) + (states('sensor.pi_hole_223_ads_blocked_today') | float)) | int }}"
      unit_of_measurement: "queries"
      icon_template: mdi:close-octagon-outline
- platform: template
  sensors:
    pi_hole_ads_percentage_blocked:
      friendly_name: "Pi-Hole Ads Percentage Blocked Today"
      unit_of_measurement: "%"
      value_template: "{{ ((states('sensor.pi_hole_222_ads_blocked_today') | float) + (states('sensor.pi_hole_223_ads_blocked_today') | float)) / ((states('sensor.pi_hole_222_dns_queries_today') | float) + (states('sensor.pi_hole_223_dns_queries_today') | float)) * 100 }}"
      icon_template: mdi:close-octagon-outline
```
