<?php
add_filter('comment_form_defaults','my_comment_form_title');
function my_comment_form_title($arg) {
		
		global $post;
		
		if (function_exists('wprs_is_enabled')) return $arg; 
		
		if (!wprs_is_enabled($post->ID)) return $arg;

		if (wprs_get_type() != 'aggregate') return $arg;
		
		$arg['title_reply'] = __('Add Review:', 'wprs');
		$arg['label_submit'] = __('Submit Review', 'wprs');
		return $arg;
}
?>
