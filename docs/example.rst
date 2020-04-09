Example Usage
=============

.. code-block:: python
   
   import asyncio
   
   from aiocf.lydia import LydiaAI
   
   
   loop = asyncio.get_event_loop()
   

   # Create Lydia instance
   # Pass an event loop to be used for aiohttp.ClientSession
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
