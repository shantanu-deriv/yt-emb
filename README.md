# YouTube embed image overlay

A tool to add more visual cue when embedding YouTube videos in GitHub.

## Run app localy

- Make sure to have [nix package manager](https://nixos.org/download.html) installed.
- Clone repo & cd into it.
- Run: `nix-shell`
- Inside the shell run `gunicorn -w 4 -b 0.0.0.0:8080 wsgi:app` and visit http://localhost:8080/

## Example

The method I used before to embed YouTube videos inside my repos was from [here](https://stackoverflow.com/questions/11804820/how-can-i-embed-a-youtube-video-on-github-wiki-pages)


For example, If I want to embed [this video](https://www.youtube.com/watch?v=3BYNj6Yvl8I) I'd use:

```
[![](http://img.youtube.com/vi/3BYNj6Yvl8I/0.jpg)](http://www.youtube.com/watch?v=3BYNj6Yvl8I "Video Title")

```

Here's how it'd look:

[![](http://img.youtube.com/vi/3BYNj6Yvl8I/0.jpg)](http://www.youtube.com/watch?v=3BYNj6Yvl8I "Video Title")

The answer above suggest that we take screen shot and embed it to make it easir to reason that the above is a video and not an image.

This tool will automate this process and add visial cues similar to an embeded youtube video.

Here's how it'd look:

[![](https://yt-emb.herokuapp.com/embed?v=3BYNj6Yvl8I)](http://www.youtube.com/watch?v=3BYNj6Yvl8I "Video Title")


```
[![](https://yt-emb.herokuapp.com/embed?v=3BYNj6Yvl8I)](http://www.youtube.com/watch?v=3BYNj6Yvl8I "Video Title")
```

## Deployment & Hosting

I used [heroku](https://heroku.com/) for deployment. The app is hosted on https://yt-emb.herokuapp.com/

