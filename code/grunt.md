### Sample Grunt TypeScript Setup

```javascript
grunt.initConfig({
  ...
  typescript: {
    base: {
      src: ['path/to/typescript/files/**/*.ts'],
      dest: 'where/you/want/your/js/files',
      options: {
        module: 'amd', //or commonjs
        target: 'es5', //or es3
        basePath: 'path/to/typescript/files',
        sourceMap: true,
        declaration: true
      }
    }
  },
  ...
});
```