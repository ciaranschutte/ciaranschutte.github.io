First few days of Toronto have flown by. I've been to two meetups already. One by Fullstack Toronto hosted by a very friendly James Wilkinson and the other at Homestars Inc, a great presentation by Luis Saffie about building an API in Rails, which I found very informative as I've only skimmed some Rails.

Although I fear a lot of what I write is already available online and this is just repetitive info I'll extract it to the interweb regardless, if only as a public log of what I'm working on.

Taking a quick break from my podcast app. Currently building a scavenger hunt app where organisers plot areas on a map with associated tasks for participants to complete. This will consist of a dashboard for organisers and a mobile app built using Ionic for the participants.

For the dashboard the user should be able to:
<ul>
	<li>create event</li>
	<ul>
		<li>create a route</li>
		<li>create markers </li>
		<li>associate task to a marker</li>
	</ul> 
	<li>view teams</li>
	<ul>
		<li>view teams task progress</li>
		<li>view where teams are</li>
	</ul>
</ul>

Nice to have would be broadcasting a message to all participants or teams.

For the app the user should be able to:
<ul>
	<li>join an event</li>
	<ul><li>create a team</li></ul>
	<li>view task</li>
	<ul><li>complete task</li></ul>
</ul>



Mapbox maps because they're really pretty, cool and customisable and I want an excuse to tweak some tile maps. I'm using <a href="https://github.com/tombatossals/angular-leaflet-directive">angular-leaflet-directive</a> for convenience. Make sure to include lat,lng AND zoom in your center variable. I had left out center and spent considerable time trying to find the issue.

{% highlight javascript %}

angular.extend($scope, {
	    defaults: {
	    	center: {
	    		lat: 53.39,
	    		lng: -6.19,
	    		zoom: 8
	    	},
	        tileLayer: "https://a.tiles.mapbox.com/v4/"+mapID+"/{z}/{x}/{y}.png?access_token="+accessToken,
	        path: {
	            weight: 10,
	            color: '#800000',
	            opacity: 1
	        }
		}
	});

{% endhighlight %}

Random thought:
It would be very cool if a high frequency sound could be emitted in a location, then the app could recognise this to provide sign up for teams. Although not sure about the implications of this on human hearing.
