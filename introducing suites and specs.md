describe("player", function() {
 var player;
 var song;

beforeEach(function() {
 player = new Player();
 song = new Song();
});

it("Should be able to play a Song", function() {
 player.play(song);
 expect(player.currentLyPlayingSong).toEqual(song);

 //demonstrates use of custom matcher
 expect(player).toBePlaying(song);
});

describe("When song has been paused", function() {
 beforeEach(function() {
  player.play(song);
  player.paused();
});