# clj-rome

A simple Clojure wrapper for the ROME feed parsing and manipulation library. Right now only the wrapper for feed parsing is implemented.

## Usage

   ;; build-feed will automaticaly dispatch on an xml string, a filepath or an url
   ;; returns a SyndFeedImpl object
   (def feed (build-feed "test/clj_rome/test/feeds/lacuisinededoria.xml"))

   ;; list-entries returns a vector of maps representing each entry
   (first (list-entries feed))
   ;; contains :contents :authors :title :link :description :categories :updated-date :published-date
   ;; the dates are in clj-time format

For more documentation on Rome, see the [ROME javadocs](http://www.jarvana.com/jarvana/view/net/java/dev/rome/rome/1.0.0/rome-1.0.0-javadoc.jar!/index.html).

## License

Copyright (C) 2011 Nils Grunwald

Distributed under the Eclipse Public License, the same as Clojure.