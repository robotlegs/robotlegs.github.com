desc 'Generate tags page'
task :tags do
  puts "Generating tags..."
  require 'rubygems'
  require 'jekyll'
  include Jekyll::Filters
  
  options = Jekyll.configuration({})
  site = Jekyll::Site.new(options)
  site.read_posts('')
  
  includes = ["community"]
    
  site.categories.sort.each do |category, posts|
    generate_page category, posts if includes.include?(category)
  end
  puts 'Done.'
end

def generate_page (category, posts)
    html = ''
    html << <<-HTML
---
layout: default
title: Postings tagged "#{category}"
---
    <h1 id="#{category}">Postings tagged "#{category}"</h1>
	HTML
	 
    html << '<ul class="posts">'
    posts.each do |post|
      post_data = post.to_liquid
      html << <<-HTML
        <li><a href="#{post.url}">#{post_data['title']}</a></li>
      HTML
    end
    html << '</ul>'
    
    File.open("tags/#{category}.html", 'w+') do |file|
      file.puts html
    end
	
end