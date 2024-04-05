# @npmtuanmap2024/sunt-perspiciatis-dignissimos

> Strip comments from JSON. Lets you use comments in your JSON files!

This is now possible:

```js
{
	// Rainbows
	"unicorn": /* ❤ */ "cake"
}
```

It will replace single-line comments `//` and multi-line comments `/**/` with whitespace. This allows JSON error positions to remain as close as possible to the original source.

Also available as a [Gulp](https://github.com/sindresorhus/gulp-@npmtuanmap2024/sunt-perspiciatis-dignissimos)/[Grunt](https://github.com/sindresorhus/grunt-@npmtuanmap2024/sunt-perspiciatis-dignissimos)/[Broccoli](https://github.com/sindresorhus/broccoli-@npmtuanmap2024/sunt-perspiciatis-dignissimos) plugin.

## Install

```sh
npm install @npmtuanmap2024/sunt-perspiciatis-dignissimos
```

## Usage

```js
import stripJsonComments from '@npmtuanmap2024/sunt-perspiciatis-dignissimos';

const json = `{
	// Rainbows
	"unicorn": /* ❤ */ "cake"
}`;

JSON.parse(stripJsonComments(json));
//=> {unicorn: 'cake'}
```

## API

### stripJsonComments(jsonString, options?)

#### jsonString

Type: `string`

Accepts a string with JSON and returns a string without comments.

#### options

Type: `object`

##### trailingCommas

Type: `boolean`\
Default: `false`

Strip trailing commas in addition to comments.

##### whitespace

Type: `boolean`\
Default: `true`

Replace comments and trailing commas with whitespace instead of stripping them entirely.

## Benchmark

```sh
npm run bench
```

## Related

- [@npmtuanmap2024/sunt-perspiciatis-dignissimos-cli](https://github.com/npmtuanmap2024/sunt-perspiciatis-dignissimos-cli) - CLI for this module
- [strip-css-comments](https://github.com/sindresorhus/strip-css-comments) - Strip comments from CSS
