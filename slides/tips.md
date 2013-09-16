<section>
	<h2>Tips 'n Tricks</h2>
    <img src="img/dude_4.gif">
</section>
<section>
	<h3>Use variables in Gruntfile.js</h3>

	<pre>
		<code  contenteditable >
		module.exports = function (grunt) {
  			var globalConfig = {
    			src: 'src',
    			dest: 'dist'
  			};
  		...
  		..
  		.
		</code>
	</pre>
	
	<pre>
		<code contenteditable >

  		jshint: {
      		all: [
      			'Gruntfile.js', '<%= globalConfig.src %>/js/{,&#42;/}&#42;.js'
      		]
      	},
    	</code>
	</pre>

</section>

<section>
	<h3>'matchdep' to load plugins</h3>

	<pre>
		<code  contenteditable >
	npm install --save-dev matchdep
		</code>
	</pre>
	
	<pre>
		<code contenteditable >
  require('matchdep').filterDev('grunt-*').forEach(grunt.loadNpmTasks);
    	</code>
	</pre>

</section>

<section>
	<h3>Alias</h3>

	<pre>
		<code  contenteditable >
	grunt.registerTask('build', [
    'clean:dist',
    'useminPrepare',
    'concat',
    'copy',
    'cssmin',
    'uglify',
    'usemin'
  ]);

  grunt.registerTask('build-with-style', [
    'jshint',
    'build'
  ]);
		</code>
	</pre>
</section>

<section>
	<h3>Command line options</h3>
	<pre>
		<code  contenteditable >
		--force
		--verbose
		--no-write
		--help
		</code>
	</pre>
</section>
<section>
	<h3>'Full stack'</h3>
	<img src="img/toolset.png">
</section>