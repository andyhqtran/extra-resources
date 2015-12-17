# Custom Dropdown

```html
<!--
  Custom Dropdown Button (http://codepen.io/andytran/pen/vLNGvN)
  Created by Andy Tran (http://andytran.me)
  Copyright 2015 Andy Tran.
  Licensed under MIT
-->

<!-- Fonts -->
<link rel='stylesheet' href='http://fonts.googleapis.com/css?family=Roboto:400,100,300,500,700,900|RobotoDraft:400,100,300,500,700,900|Material+Icons:%20400' type='text/css' media='all' />

<!-- Styles -->
<style>
  .custom--btn-container {
    z-index: 100;
    position: relative;
    display: inline-block;
  }

  .custom--btn {
    outline: 0;
    display: -webkit-inline-box;
    display: -webkit-inline-flex;
    display: -ms-inline-flexbox;
    display: inline-flex;
    -webkit-box-align: center;
    -webkit-align-items: center;
        -ms-flex-align: center;
            align-items: center;
    -webkit-box-pack: justify;
    -webkit-justify-content: space-between;
        -ms-flex-pack: justify;
            justify-content: space-between;
    background: #5380F7;
    min-width: 260px;
    border: 0;
    border-radius: 4px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    box-sizing: border-box;
    padding: 16px 20px;
    color: #FFFFFF !important;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 1.2px;
    text-transform: uppercase;
    overflow: hidden;
    cursor: pointer;
  }
  .custom--btn:hover {
    background: #3b6ef6;
  }
  .custom--btn:focus .dropdown, .custom--btn:active .dropdown {
    -webkit-transform: translate(0, 20px);
            transform: translate(0, 20px);
    opacity: 1;
    visibility: visible;
  }
  .custom--btn .material-icons {
    border-radius: 100%;
    -webkit-animation: ripple 0.6s linear infinite;
            animation: ripple 0.6s linear infinite;
  }
  .custom--btn .dropdown {
    position: absolute;
    top: 100%;
    left: 0;
    list-style: none;
    background: #FFFFFF;
    width: 100%;
    padding: 0;
    border-radius: 4px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    text-align: left;
    opacity: 0;
    visibility: hidden;
    -webkit-transition: 0.3s ease;
    transition: 0.3s ease;
  }
  .custom--btn .dropdown:before {
    content: '';
    position: absolute;
    top: -6px;
    left: 20px;
    width: 0;
    height: 0;
    box-shadow: 2px -2px 6px rgba(0, 0, 0, 0.05);
    border-top: 6px solid #FFFFFF;
    border-right: 6px solid #FFFFFF;
    border-bottom: 6px solid transparent;
    border-left: 6px solid transparent;
    -webkit-transform: rotate(-45deg);
            transform: rotate(-45deg);
    mix-blend-mode: multiple;
  }
  .custom--btn .dropdown li {
    z-index: 1;
    position: relative;
    background: #FFFFFF;
    margin: 0;
    padding: 0 20px;
    color: #666;
  }
  .custom--btn .dropdown li.active {
    color: #5380F7;
  }
  .custom--btn .dropdown li:first-child {
    border-radius: 4px 4px 0 0;
  }
  .custom--btn .dropdown li:last-child {
    border-radius: 0 0 4px 4px;
  }
  .custom--btn .dropdown li:last-child a {
    border-bottom: 0;
  }
  .custom--btn .dropdown a {
    display: block;
    border-bottom: 1px solid rgba(0, 0, 0, 0.05);
    padding: 16px 0;
    color: inherit;
    font-size: 10px;
    text-decoration: none;
  }

  @-webkit-keyframes ripple {
    0% {
      box-shadow: 0 0 0 0 rgba(255, 255, 255, 0.1), 0 0 0 20px rgba(255, 255, 255, 0.1), 0 0 0 40px rgba(255, 255, 255, 0.1), 0 0 0 60px rgba(255, 255, 255, 0.1);
    }
    100% {
      box-shadow: 0 0 0 20px rgba(255, 255, 255, 0.1), 0 0 0 40px rgba(255, 255, 255, 0.1), 0 0 0 60px rgba(255, 255, 255, 0.1), 0 0 0 80px rgba(255, 255, 255, 0);
    }
  }

  @keyframes ripple {
    0% {
      box-shadow: 0 0 0 0 rgba(255, 255, 255, 0.1), 0 0 0 20px rgba(255, 255, 255, 0.1), 0 0 0 40px rgba(255, 255, 255, 0.1), 0 0 0 60px rgba(255, 255, 255, 0.1);
    }
    100% {
      box-shadow: 0 0 0 20px rgba(255, 255, 255, 0.1), 0 0 0 40px rgba(255, 255, 255, 0.1), 0 0 0 60px rgba(255, 255, 255, 0.1), 0 0 0 80px rgba(255, 255, 255, 0);
    }
  }
</style>

<div class="custom--btn-container">
  <!-- Btn-->
  <button class="custom--btn">
    <span>Account Settings</span>
    <i class="material-icons">public</i>

    <ul class="dropdown">
      <li class="active"><a href="http://andytran.me">Profile Information</a></li>
      <li><a href="http://andytran.me">Change Password</a></li>
      <li><a href="http://codepen.io/pro">Become <b>PRO</b></a></li>
      <li><a href="http://andytran.me">Help</a></li>
      <li><a href="http://andytran.me">Log Out</a></li>
    </ul>
  </button>
</div>

<!-- Scripts -->
<script>
</script>```