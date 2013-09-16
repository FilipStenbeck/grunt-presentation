<section>
	<h2>Easy to configure</h2>
    <img src="img/dude_2.gif">
</section>
<section>
	<img src="img/gruntfile.png"/>
</section>

<section>
	<pre>
		<code data-trim contenteditable >
			module.exports = function(grunt) {
 				grunt.initConfig({
 					...
 					..
 					.
 				}
 			}; 
		</code>
	</pre>
</section>
<section>
	<pre>
		<code data-trim contenteditable >
			concat: {
				dist: {
				    src: ['js/a.js', 'js/b.js', 'js/c.js'],
				    dest: 'dist/js/app.js'
			 	}
			}
		</code>
	</pre>
</section>
<section>
	<pre>
		<code data-trim contenteditable >
			uglify: {
			  dist: {
			    files: {
			      'dist/js/app-min.js': ['dist/js/app.js' ]
			    }
			  }
			 }
		</code>
	</pre>
</section>
<section>
	<pre>
		<code  contenteditable >
			grunt.loadNpmTasks('grunt-contrib-concat');
			grunt.loadNpmTasks('grunt-contrib-uglify');

			grunt.registerTask('build', ['concat','uglify']);
		</code>
	</pre>
</section>
