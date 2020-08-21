# How to use spys one proxy list

## Installation:
```pip install spys1proxy```

## Taking any proxy list:

```
from spys1proxy import Spys

spys_one = Spys(any_country=True)
await spys_one.search()
```
## Taking only europe list:
```spys_one = Spys(europe=True)```
## Taking North America list:

```spys_one = Spys(north_america=True)```

## Taking ips from chosen countries:

```spys_one = Spys(countries=['DE', 'PL', 'NL'])```

### Getting results:
   *   After ```await spys_one.search()``` you should able to watch list of lists in
   `spys_one.proxy_list`
   * Run `search()` in awaitable coroutine or with asyncio loop.run_until_complete

```   
    loop = asyncio.get_event_loop()
    spys = Spys()
    spys.countries.append('DE')
    loop.run_until_complete(spys.search())
    print(spys, spys.proxy_list)
```
        