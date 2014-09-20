<?php

/**
 * support: do-right@mail.ru
 */

if (file_exists('../../config.php')) {
    require_once('../../config.php');
}

require_once(DIR_SYSTEM . 'startup.php');

$db = new DB(DB_DRIVER, DB_HOSTNAME, DB_USERNAME, DB_PASSWORD, DB_DATABASE);
$query = $db->query("CREATE TABLE IF NOT EXISTS `". DB_PREFIX ."review_image` (
  `review_image_id` int(11) NOT NULL AUTO_INCREMENT,
  `review_id` int(11) NOT NULL,
  `image` varchar(255) DEFAULT NULL,
  `sort_order` int(3) NOT NULL DEFAULT '0',
  PRIMARY KEY (`review_image_id`)
) ENGINE=MyISAM  DEFAULT CHARSET=utf8 AUTO_INCREMENT=1 ;");

$query = $db->query("SHOW TABLES FROM ". DB_DATABASE ." LIKE '". DB_PREFIX ."review_image';");
if (!$query->num_rows) {
    exit('Error. Table `review_image` not found');
} else {
    exit('Module has been installed successfully! <a href="/">Index Page</a>');
}
