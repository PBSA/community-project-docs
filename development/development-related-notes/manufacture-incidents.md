# Manufacture Incidents

```text
"_Baseball__MLB__New York Yankees__Minnesota Twins_": 
All eventgroups finished before 2020. 
Add a new event group in bookie sports

```

### 

### Important

1. Remotes are dumb. As long as format matches, they will produce incidents. It's the responsibility of bookiesports to makesure whether such an incidents is possible.
2. Dataproxy, BLKCHND: We don't own it. We have limited access.

The corresponding code shall be made available in bos-utils

### Working Remotes

#### ScorePro / BLKCHND Not working now

{% embed url="https://174.138.14.239:8010" %}

7903ac4b2b8c6486f2a56c7313e4d80b

#### Lsports / Omni

149.56.89.138:8010

{% embed url="https://dp0.omnidata.tech:8010" %}

612da494e7960539e8e45104c9a5fca2

### Non Working Remotes

#### Enetpulse

{% embed url="https://95.216.13.245:8010" %}

d28654530fb07360f051c713bdd749bb

### Create event \(atleast 2 required\)

[http://174.138.14.239:8010/replay?token=pbsabookie&restrict\_witness\_group=elizabeth&manufacture=2020-04-01T20:00:00Z\_\_Soccer\_\_SerieA\_\_Bologna\_\_Cagliari\_\_create\_\_2020](http://174.138.14.239:8010/replay?token=pbsabookie&restrict_witness_group=elizabeth&manufacture=2020-04-01T20:00:00Z__Soccer__SerieA__Bologna__Cagliari__create__2020) 

[http://149.56.89.138:8010/replay?token=pbsabookie&restrict\_witness\_group=elizabeth&manufacture=2020-04-01T20:00:00Z\_\_Soccer\_\_SerieA\_\_Bologna\_\_Cagliari\_\_create\_\_2020](http://149.56.89.138:8010/replay?token=pbsabookie&restrict_witness_group=elizabeth&manufacture=2020-04-01T20:00:00Z__Soccer__SerieA__Bologna__Cagliari__create__2020) 

[http://dp0.omnidata.tech:8010/replay?token=pbsabookie&restrict\_witness\_group=elizabeth&manufacture=2020-04-01T20:00:00Z\_\_Soccer\_\_SerieA\_\_Bologna\_\_Cagliari\_\_create\_\_2020](http://dp0.omnidata.tech:8010/replay?token=pbsabookie&restrict_witness_group=elizabeth&manufacture=2020-04-01T20:00:00Z__Soccer__SerieA__Bologna__Cagliari__create__2020) 

### Event start \(one incident\)

[http://174.138.14.239:8010/replay?token=pbsabookie&restrict\_witness\_group=elizabeth&manufacture=2020-04-01T20:00:00Z\_\_Soccer\_\_SerieA\_\_Bologna\_\_Cagliari\_\_in\_progress\_\_2020-04-01T200000z](http://174.138.14.239:8010/replay?token=pbsabookie&restrict_witness_group=elizabeth&manufacture=2020-04-01T20:00:00Z__Soccer__SerieA__Bologna__Cagliari__in_progress__2020-04-01T200000z)

[http://149.56.89.138:8010/replay?token=pbsabookie&restrict\_witness\_group=elizabeth&manufacture=2020-04-01T20:00:00Z\_\_Soccer\_\_SerieA\_\_Bologna\_\_Cagliari\_\_in\_progress\_\_2020-04-01T210000z](http://149.56.89.138:8010/replay?token=pbsabookie&restrict_witness_group=elizabeth&manufacture=2020-04-01T20:00:00Z__Soccer__SerieA__Bologna__Cagliari__in_progress__2020-04-01T210000z)

### Result, \(atleast 2 incidents required\)

[http://174.138.14.239:8010/replay?token=pbsabookie&restrict\_witness\_group=elizabeth&manufacture=2020-04-01T20:00:00Z\_\_Soccer\_\_SerieA\_\_Bologna\_\_Cagliari\_\_result\_\_2\_\_3](http://174.138.14.239:8010/replay?token=pbsabookie&restrict_witness_group=elizabeth&manufacture=2020-04-01T20:00:00Z__Soccer__SerieA__Bologna__Cagliari__result__2__3)

[http://149.56.89.138:8010/replay?token=pbsabookie&restrict\_witness\_group=elizabeth&manufacture=2020-04-01T20:00:00Z\_\_Soccer\_\_SerieA\_\_Bologna\_\_Cagliari\_\_result\_\_2\_\_3](http://149.56.89.138:8010/replay?token=pbsabookie&restrict_witness_group=elizabeth&manufacture=2020-04-01T20:00:00Z__Soccer__SerieA__Bologna__Cagliari__result__2__3)



### Working Events

```text
"_Soccer__SerieA__Bologna__Cagliari_",
"_Soccer__Epl__Chelsea__Brighton_",
"_Soccer__SerieA__Lazio__Parma_",
"_Basketball__NBA Playoffs__Orlando Magic__Toronto Raptors_",

```

### Events with Normalisation Error

```text
"_Baseball__MLB__New York Yankees__Minnesota Twins_": 
"_basketball__nba-regular-season__Booklyn-Nets__Detroit-Pistons_", 
"_Basketball__NBA Playoffs__Orlando Magic__Toronto Raptors_",
"_Basketball__NBA Playoffs__Orlando Magic__Toronto Raptors_",
"_Baseball__MLB__Los Angeles Angels__Oakland Athletics_",
"_Baseball__MLB__San Francisco Giants__Arizona Diamondbacks_",
"_Baseball__MLB__Los Angeles Angels__Oakland Athletics_"
```

### Wrong Event

```text
"_mlb-regular-season__tampa-bay-rays__new-york-yankees_",

```

### Version Notes

Elizabeth, machine 242, bookiesports version: Name: bookiesports Version: 0.4.14



