Partition Gallery
=================
A jQuery plugin for generating a balanced photo gallery. Based on
[this article](http://www.crispymtn.com/stories/the-algorithm-for-a-perfectly-balanced-photo-gallery).

Example
=======
    var images = $("#gallery img");
    var length = images.length;
    var loaded = 0;
    images.each(function () {
      $(this).bind('load', function () {
        if ((++loaded) === length)
          $("#gallery").partitionGallery(images);
     });
  });
