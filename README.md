# CakePHPAuth

CakePHPAuth is CakePHP + Auth component. 

It also includes user views (add/login/logout/view/index etc.)


It's based on [CakeStrap from HugoDias](http://www.github.com/hugodias/cakeStrap) - which is a great BootStrap/CakePHP mashup - but some people prefer to start with their own views.

It also includes a unix_socket in the database.php in case you're using MAMP.

## Installation
Clone the project:
`git clone http://github.com/itamark/CakePHPAuth.git`

Set up the Database and users tabel by running this SQL:

        SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
        SET time_zone = "+00:00";
        
        --
        -- Database: `CakePHPAuth`
        --
        CREATE DATABASE IF NOT EXISTS `CakePHPAuth` DEFAULT CHARACTER SET latin1 COLLATE latin1_swedish_ci;
        USE `CakePHPAuth`;
        
        -- --------------------------------------------------------
        
        --
        -- Table structure for table `users`
        --
        
        DROP TABLE IF EXISTS `users`;
        CREATE TABLE IF NOT EXISTS `users` (
          `id` int(11) NOT NULL AUTO_INCREMENT,
          `username` varchar(255) NOT NULL,
          `password` varchar(255) NOT NULL,
          `email` varchar(225) NOT NULL,
          `name` varchar(255) NOT NULL,
          `role` varchar(20) NOT NULL,
          `created` datetime NOT NULL,
          `modified` datetime NOT NULL,
          PRIMARY KEY (`id`)
        ) ENGINE=InnoDB  DEFAULT CHARSET=latin1 AUTO_INCREMENT=7 ;


After creating your first user, you'll have to manually go in to the database and set `role` to `admin` to get access to admin rights.
