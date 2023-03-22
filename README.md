# Spotify API
This is a Rust project that provides a simple interface to search for tracks, albums, artists and playlists on the Spotify API. It allows users to easily search for music using various parameters such as track title, artist name, album name, genre and more.

## Usage
To get a free token from Spotify: [Search for Item](https://developer.spotify.com/console/get-search-item/?q=Muse&type=track&market=US&limit=5&offset=5&include_external=)
```
cargo run "[search query]" "[Spotify auth token]"
```
Here is an example of how to use Rust-Spotify-API-Search to search for a track:
```
use spotify_api_search::SpotifyClient;
use spotify_api_search::types::SearchType;

fn main() {
    let client = SpotifyClient::new("YOUR_ACCESS_TOKEN".to_string());
    let query = "Lose Yourself";
    let search_type = SearchType::Track;
    let result = client.search(query, search_type);
    println!("{:?}", result);
}
```
The above example creates a new `SpotifyClient` with your access token, then searches for a track with the title "Lose Yourself". The search type is set to `SearchType::Track` to indicate that we are searching for a track.

## References

* [rust-cli-template](https://github.com/kbknapp/rust-cli-template)
