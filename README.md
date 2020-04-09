# Asynchronous CoffeeHouse API Wrapper for Python

This is a very simple API Wrapper for the CoffeeHouse API. Using
This Library only supports the V1IVA2.0 CoffeeHouse API which is based from
this [Documentation](https://gist.github.com/Netkas/e8977b26f482ca40911a949df7dd286f)


## Installation
```sh
pip install aiocf
```

or
```sh
python setup.py build
python setup.py install
```

## Requirements
• Python 3.5.3+


## Lydia Example

```import asyncio
   
from aiocf.lydia import LydiaAI
   

loop = asyncio.get_event_loop()
   

# Create Lydia instance
# Pass an event loop to be used for aiohttp.ClientSession
# You could also pass a ClientSession as the session keyword argument
# If no loop is passed, asyncio.get_event_loop() is called
lydia = LydiaAI("<YOUR API KEY>", loop=loop)
   

async def main():
    session = await lydia.create_session()
    while True:
    output = await session.think_thought(input("Input: "))
    print(f"Output: {output}")
    

if __name__ == "__main__":
    try:
        loop.run_until_complete(main())
    finally:
        loop.run_until_complete(lydia.close()) # Close aiohttp.ClientSession
```
