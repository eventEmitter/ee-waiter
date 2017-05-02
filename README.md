# parallel control flow library

[![Greenkeeper badge](https://badges.greenkeeper.io/eventEmitter/ee-waiter.svg)](https://greenkeeper.io/)


	var Waiter = require( "ee-waiter" );


	var waiter = new Waiter( function( err ){
		if ( err ) console.log( "there was an erorr:", err );
		...
	} );


	waiter.add( function( cb ){
		// do something ..
		cb();
	} );

	waiter.add( function( cb ){
		// do something ..
		cb();
	} );


	// start all previosuly defined jobs in parallel
	waiter.start();