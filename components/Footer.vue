<template>
	<div>
		 
	</div>
  </template>
  
  <style>
	  footer {
		  /* background-color: var(--clr-blue-600); */
	  }
  
	  .footer-content {
		  display: flex;
		  flex-direction: row;
		  max-width: 100%;
		  flex-shrink: 7;
		  padding-bottom: 2rem;
		  justify-content: space-evenly;
		  gap: 0.5rem
	  }
  
	  .footer-content div {
		  margin-bottom: 2rem;
	  }
  
	  @media (min-width: 1024px) {
		  .footer-content {
			  flex-direction: row;
		  }
  
		  .footer-content div {
			  margin-right: 2rem;
			  min-width: 12rem;
		  }
	  }
  
	  .social-links {
		  display: flex;
		  flex-direction: column;
		  
	  }
  
	  .link-icon {
		  width: 1rem;
		  margin-right: 0.5rem;
		  color: var(--clr-white);
	  }
  
	  .link-text {
		  color: var(--clr-white);
		  font-weight: 500;
		  display: flex;
		  align-items: center;
		  margin-bottom: 0.5rem;
		  transition: color 0.2s;
		  line-height: 1rem;
	  }
  
	  .link-text:hover {
		  color: var(--clr-yellow);
	  }
  
	  address {
		  font-style: normal;
	  }
  
  </style>