https://wordpress.stackexchange.com/questions/30039/how-to-display-related-posts-from-same-category


  <?php
$related = get_posts( 
    array( 
        'category__in' => wp_get_post_categories( $post->ID ), 
        'numberposts'  => 5, 
        'post__not_in' => array( $post->ID ) 
    ) 
);

//print_r($related); 
?>

  <div class="popular-products-section padd46px">
    <div class="container">
      <h2 class="subheading-orang margenbt30 text-center">Related Post</h2>
      <div class="popular-list">
        <div class="owl-carousel owl-theme">
          <?php      if( $related ) { 
    foreach( $related as $post ) {
        setup_postdata($post); ?>
           <div class="item">

            <figure>
             <?php if ( has_post_thumbnail() ) { ?>
              <?php echo get_the_post_thumbnail(); ?>
              
            <?php } else { echo get_the_post_thumbnail();
              echo '<img src="'.get_template_directory_uri().'/images/no-img/210x204.png" alt="'.get_the_title().'" title="'.get_the_title().'">';
              } ?>
            </figure>
            
            <div class="content">
              <h3><a href="<?php echo get_permalink(); ?>"><?php echo get_the_title(); ?></a></h3>
              <div class="datainfo">
                <p><?php echo tm_excerpt(get_the_content(), 75); ?></p>
              </div>
            </div>
            <p class="linkbtn"><a href="<?php echo get_permalink(); ?>">View Detail <i class="fa fa-fw"></i></a></p>
          </div>
                       <?php     }
    wp_reset_postdata();
} ?>

        </div>

      </div>

      <script type="text/javascript">

                jQuery(document).ready(function(e) {
                    jQuery('.popular-list .owl-carousel').owlCarousel({
                    loop:false,
                    margin:28, dots: false,
                    responsiveClass:true,  items:4,
                    responsive:{
                        0:{
                            items:1,
                            nav:false
                        },
                        640:{
                            items:2,
                            nav:false,
                            margin:10                           
                        },
                        768:{
                            items:3,
                            nav:true,
                            margin:10                           
                        },

                        992:{
                            items:3,
                            nav:true,
                            margin:30

                        },

                        1200:{
                            nav:true
                        }
                    }
                    })
                });
                </script> 
    </div>
  </div>
