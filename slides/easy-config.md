<section>
	<h2>Enkelt att konfigurera</h2>
</section>
<section>
	<img src="img/gruntfile.png"/>
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
				      'dist/js/app.js': ['dist/js/app.js' ]
				    }
				  }
				 }
			</code>
		</pre>
</section>
<section>  
  <ol>
    <li class="extra-extra-spacing">grunt.loadNpmTasks('grunt-contrib-uglify'); </li>
    <li class="extra-extra-spacing">grunt.registerTask('build', ['concat','uglify']); </li>
    <li class="extra-extra-spacing"> grunt.registerTask('default', ['build']);</li>
   <ol>
</section>

