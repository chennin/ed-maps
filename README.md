Holding some files used for mapping

Crystalline Shard sites: https://edastro.com/galmap/?custom=https://raw.githubusercontent.com/chennin/ed-maps/main/cs.json

  From Canonn's spreadsheet

Ringed Neutrons: https://edastro.com/galmap/?custom=https://raw.githubusercontent.com/chennin/ed-maps/main/ringed-neutron.json

  Generated with the following (incomplete) command -- requires text replacement too. Neutron dump from https://edastro.com/mapcharts/files.html

  `csvgrep  -c 14 -r "[1-9]" dump-neutron-star.csv | csvcut -c 9,37,38,39 | csvjson >> ringed-neutron.json`

Thargoids: https://edastro.com/galmap/?custom=https://raw.githubusercontent.com/chennin/ed-maps/main/thargoid.json

  Generated half with the following, using https://edastro.com/mapcharts/files/codex-data.csv:

  `csvgrep -c 1 -r "Thargoid" codex-data.csv | csvcut -c 1,6,7,8,9 | csvjson | jq -r . > thargoid.json`
