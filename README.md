
# The Climate Change News API
The climate change API si a simple `REST API` that allows you to consume all the current news that contain the word 'climate' in their title from different important news sites from all around the world.

### Endpoints

    GET -> https://news-about-climate-change-api.herokuapp.com/news
*This endpoint will return a list of all the news articles available, crawled from the list of news websites at the moment of the request.*

    https://news-about-climate-change-api.herokuapp.com/news/:newspaperId
*This endpoint allows you to specify a specific source from where the API should return news articles. The newspaper ID can be found at the bottom as the name property of each newspaper object.*

**All responses from the API are returned as JSON in the following format: An Array containg Objects for each individual news story (see example below).**

      [
	      {
	        "title": "How war has upended life for climate activists in Russia“It’s kind of difficult to be afraid all the time that someone might knock down your door,” one said.By Manuela Andreoni",
	        "url": "https://www.nytimes.com/2022/04/01/climate/ukraine-war-climate-activists.html",
	        "source": "nyt"
	      },
	      {
	        "title": "Here’s what Biden’s budget would do, and not do, for climate changeThe president’s federal spending proposal for the next year contains almost $45 billion to deal with global warming. We looked at the details.By Somini Sengupta",
	        "url": "https://www.nytimes.com/2022/03/29/climate/biden-budget-climate.html",
	        "source": "nyt"
	      },
	      {
	        "title": "@nytclimatetwitter page for @nytclimate",
	        "url": "https://www.nytimes.comhttps://twitter.com/nytclimate",
	        "source": "nyt"
	      }
    ]

The list of all the possible sources can be found below:

    [
    
      {
        name: 'cityam',
        address: 'https://www.cityam.com/london-must-become-a-world-leader-on-climate-change-action/',
        base: ''
      },

      {
        name: 'thetimes',
        address: 'https://www.thetimes.co.uk/environment/climate-change',
        base: ''
      },

      {
        name: 'guardian',
        address: 'https://www.theguardian.com/environment/climate-crisis',
        base: '',
      },

      {
        name: 'telegraph',
        address: 'https://www.telegraph.co.uk/climate-change',
        base: 'https://www.telegraph.co.uk',
      },

      {
        name: 'nyt',
        address: 'https://www.nytimes.com/international/section/climate',
        base: 'https://www.nytimes.com',
      },

      {
        name: 'latimes',
        address: 'https://www.latimes.com/environment',
        base: '',
      },

      {
        name: 'smh',
        address: 'https://www.smh.com.au/environment/climate-change',
        base: 'https://www.smh.com.au',
      },

      {
        name: 'un',
        address: 'https://www.un.org/climatechange',
        base: '',
      },

      { 
        name: 'bbc',
        address: 'https://www.bbc.co.uk/news/science_and_environment',
        base: 'https://www.bbc.co.uk',
      },

      {
        name: 'es',
        address: 'https://www.standard.co.uk/topic/climate-change',
        base: 'https://www.standard.co.uk'
      },

      {
        name: 'sun',
        address: 'https://www.thesun.co.uk/topic/climate-change-environment/',
        base: ''
      },

      {
        name: 'dm',
        address: 'https://www.dailymail.co.uk/news/climate_change_global_warming/index.html',
        base: ''
      },

      {
        name: 'nyp',
        address: 'https://nypost.com/tag/climate-change/',
        base: ''
      },

      {
        name: 'independent',
        address: 'https://www.independent.co.uk/climate-change',
        base: 'https://www.independent.co.uk'
      },

      {
        name: 'sky',
        address: 'https://news.sky.com/climate',
        base: 'https://news.sky.com'
      },

      {
        name: 'vox',
        address: 'https://www.vox.com/energy-and-environment',
        base: 'https://www.vox.com'
      }
    
    ]


