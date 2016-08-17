$(function () {
  var weather, feed, title, content,
    rss = 'http://weather.yahooapis.com/forecastrss?w=2306180&u=c',
    url = 'https://ajax.googleapis.com/ajax/services/feed/load?v=1.0&callback=?&q=' + encodeURIComponent(rss);
  $.ajax({
    type: "GET",
    url: url,
    dataType: "json",
    error: function (e) {
      console.log('oh no');
    },
    success: function (e) {
      weather = $(e);
      feed = weather[0].responseData.feed;
      console.log(weather);
      console.log(feed);
      title = feed.title;
      content = feed.entries[0].content;
      $('h3').append(title);
      $('.ui-content').append(content);
    }
  });
});