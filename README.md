# react-custom-scrollbars-4

[![npm](https://img.shields.io/badge/npm-react--custom--scrollbars--4-brightgreen.svg?style=flat-square)](https://www.npmjs.com/package/react-custom-scrollbars-4)
[![npm version](https://img.shields.io/npm/v/react-custom-scrollbars-4.svg?style=flat-square)](https://www.npmjs.com/package/react-custom-scrollbars-4)
[![npm downloads](https://img.shields.io/npm/dm/react-custom-scrollbars-4.svg?style=flat-square)](https://www.npmjs.com/package/react-custom-scrollbars-4)

- frictionless native browser scrolling
- native scrollbars for mobile devices
- [fully customizable](https://github.com/barrenechea/react-custom-scrollbars-4/wiki/Customization)
- [auto hide](https://github.com/barrenechea/react-custom-scrollbars-4/wiki/Usage#auto-hide)
- [auto height](https://github.com/barrenechea/react-custom-scrollbars-4/wiki/Usage#auto-height)
- [universal](https://github.com/barrenechea/react-custom-scrollbars-4/wiki/Usage#universal-rendering) (runs on client & server)
- `requestAnimationFrame` for 60fps
- no extra stylesheets
- well tested, 100% code coverage

**[Demos](https://robpethick.github.io/react-custom-scrollbars-2/) · [Wiki](https://github.com/barrenechea/react-custom-scrollbars-4/wiki)**

## Quick note

This repo is due to both the original [`react-custom-scrollbars`](https://www.npmjs.com/package/react-custom-scrollbars) and [`react-custom-scrollbars-2`](https://www.npmjs.com/package/react-custom-scrollbars-2) packages being stale. Initially to add React 19 support, this fork aims to modernize it in every way, while keeping the original APIs intact.

## Installation

```bash
npm install react-custom-scrollbars-4
```

This assumes that you’re using [npm](https://www.npmjs.com) package manager with a module bundler like [Vite](https://vite.dev) or [Webpack](https://webpack.js.org) to consume [CommonJS modules](https://webpack.js.org/api/module-methods/#commonjs).

If you don’t yet use [npm](https://www.npmjs.com) or a modern module bundler, and would rather prefer a single-file [UMD](https://github.com/umdjs/umd) build that makes `ReactCustomScrollbars` available as a global object, you can grab a pre-built version from [unpkg](https://unpkg.com/react-custom-scrollbars-4@4.5.1/dist/react-custom-scrollbars.js). We _don’t_ recommend this approach for any serious application, as most of the libraries complementary to `react-custom-scrollbars-4` are only available on [npm](https://www.npmjs.com).

## Usage

This is the minimal configuration. [Check out the Wiki for advanced usage](https://github.com/barrenechea/react-custom-scrollbars-4/wiki).

```tsx
import { Scrollbars } from "react-custom-scrollbars-4";

const App = () => {
  return (
    <Scrollbars style={{ width: 500, height: 300 }}>
      <p>Some great content...</p>
    </Scrollbars>
  );
};
```

The `<Scrollbars>` component is completely customizable. Check out the following code:

```tsx
import { Scrollbars } from 'react-custom-scrollbars-4';

class CustomScrollbars extends Component {
  render() {
    return (
      <Scrollbars
        onScroll={this.handleScroll}
        onScrollFrame={this.handleScrollFrame}
        onScrollStart={this.handleScrollStart}
        onScrollStop={this.handleScrollStop}
        onUpdate={this.handleUpdate}
        renderView={this.renderView}
        renderTrackHorizontal={this.renderTrackHorizontal}
        renderTrackVertical={this.renderTrackVertical}
        renderThumbHorizontal={this.renderThumbHorizontal}
        renderThumbVertical={this.renderThumbVertical}
        autoHide
        autoHideTimeout={1000}
        autoHideDuration={200}
        autoHeight
        autoHeightMin={0}
        autoHeightMax={200}
        thumbMinSize={30}
        universal={true}
        {...this.props}>
    );
  }
}
```

All properties are documented in the [Wiki](https://github.com/barrenechea/react-custom-scrollbars-4/wiki/API)

## Examples

Run the simple example:

```bash
# Make sure that you've installed the dependencies
npm install
# Move to example directory
cd react-custom-scrollbars-4/examples/simple
npm install
npm start
```

## Tests

```bash
# Make sure that you've installed the dependencies
npm install
# Run tests
npm test
```

### Code Coverage

```bash
# Run code coverage. Results can be found in `./coverage`
npm run test:cov
```

## License

MIT
