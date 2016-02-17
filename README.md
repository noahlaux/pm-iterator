# pm-iterator

`<pm-iterator>` cycles through values between a two bounderies, optionally using butter smooth timed tweening with easings. You can control how many times it should perform the cycle and get notified about iteration life-cycles.

__Perfect for:__

  * Auto advance slideshows
  * Spiffy animated counters
  * Composing complex animations declaratively
  * ...anywhere your mind takes you (plz, keep it private!)

#### Example for driving a slideshow:
	```html
    <pm-iterator
      min="0"
      max="5"
      duration="5000"
      times="Infinite"
      value="{{ selected }}">
    </pm-iterator>

    <neon-animated-pages
      selected="[[ selected ]]">
      <neon-animatable>Slide1</neon-animatable>
      ...
    </neon-animated-pages>
    ```

#### Example animating a box:

	```html
    <pm-iterator
      value="{{ xValue }}"
      min="0"
      max="100"
      duration="2000"
      is-end="{{ isEnd }}"
      easing="easeOutBounce"
      times="5"></pm-iterator>

    <div
      class="cube"
      end$="[[ isEnd ]]"
      style="transform: translateX([[ xValue ]]px);"></div>
     ```

# Available easings

  * linear
  * easeInQuad
  * easeOutQuad
  * easeInOutQuad
  * easeInCubic
  * easeOutCubic
  * easeInOutCubic
  * easeInQuart
  * easeOutQuart
  * easeInOutQuart
  * easeInQuint
  * easeOutQuint
  * easeInOutQuint
  * easeInSine
  * easeOutSine
  * easeInOutSine
  * easeInExpo
  * easeOutExpo
  * easeInOutExpo
  * easeInCirc
  * easeOutCirc
  * easeInOutCirc
  * easeInElastic
  * easeOutElastic
  * easeInOutElastic
  * easeInBack
  * easeOutBack
  * easeInOutBack
  * easeInBounce
  * easeOutBounce
  * easeInOutBounce

## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install


## Playing With Your Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polyserve

And you can run it via:

    polyserve

Once running, you can preview your element at
`http://localhost:8080/components/pm-iterator/`, where `pm-iterator` is the name of the directory containing it.


## Testing Your Element

Simply navigate to the `/test` directory of your element to run its tests. If
you are using Polyserve: `http://localhost:8080/components/pm-iterator/test/`

### web-component-tester

The tests are compatible with [web-component-tester](https://github.com/Polymer/web-component-tester).
Install it via:

    npm install -g web-component-tester

Then, you can run your tests on _all_ of your local browsers via:

    wct

#### WCT Tips

`wct -l chrome` will only run tests in chrome.

`wct -p` will keep the browsers alive after test runs (refresh to re-run).

`wct test/some-file.html` will test only the files you specify.


## Yeoman support

If you'd like to use Yeoman to scaffold your element that's possible. The official [`generator-polymer`](https://github.com/yeoman/generator-polymer) generator has a [`seed`](https://github.com/yeoman/generator-polymer#seed) subgenerator.
