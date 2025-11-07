# CHANGELOG – Wedding AI Taxonomy

## v1.3 (2025-11-05)
- Added conversational_behavior.* (detect_city_soft, allow_cross_city, user_message.*)
- Added capacity_fit.user_message.capacity.* (under/ideal/over)
- Added venue.has_ceremony_space in venue.fields
- Added venue.menu_quality.inputs.*
- Added decor.candybar_quality.inputs.*
- Added fx.effects_and_lighting.interpret.*
- Added general_policies.cancel_policy and general_policies.accessibility
- Added explain_compare.custom_comment


## v1.4 (2025-11-05)
- photo_video.fields: added `team_years_experience`, `team_events_per_year`
- photo_video.deliverables: added `delivery_times_combined`
- vendor_schema.scoring: added `price_value_ratio` (global efficiency metric)
- ruleset_metadata.keys: added `budget_rule` (conditional recommendation threshold key)

## v1.5 (2025-11-06)
- decor.inputs.optional: added `weather_risk`, `inclus_bouquet`
- enums: added `weather_risk` = [low, medium, high], `decor_volume` = [small, medium, full]
- decor.decision_tree.computed: added `decor_volume`
- decor.synergies.with_photo_video_FV.flags: added `photo_friendly`
- decor.budget.pricing_model: added `urgency_fee`

## v1.6 (2025-11-06)
- fx.extensions: added `show_density` (enum: low, medium, high) + enums.show_density
- fx.compat: added `requires_venue_allows_heavy_smoke` (bool), `requires_venue_allows_cold_spark` (bool),
  `safety_distance_m` (int), `permits_required` (bool), `permit_lead_days` (int),
  `weather_risk` (enum ref), `noise_curfew_time` (HH:MM)

## v1.7 (2025-11-07)
At transport category
- Added  
pricing:
    - name: base_price_eur
      type: float
    - name: price_per_km_eur
      type: float
    - name: ac_included
      type: bool
      description: Indică dacă aerul condiționat este inclus în prețul de bază al transportului.
      default: false
    - name: ac_fee_eur_fixed
      type: float
      description: Taxă fixă suplimentară pentru aer condiționat, stabilită de furnizor (nu pe oră).
      default: 0.0

## v1.8 (2025-11-08)
### Added – Derived fields for venue comparisons
- `capacity_fit.level` → ratio-based label (low/medium/high)
- `dancefloor_fit.level` → derived from dancefloor size + event style
- `curfew_impact.level` → derived from curfew time
- `distance_convenience.band` → derived from km/time
- `min_guarantee_policy.value` → numeric minimum seats guarantee
- `cross_city_suggested` → flag for “better venue outside preferred city”
