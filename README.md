# disable_back_and_F5_on_browser
Conatains javascript code to disable browser back and F5 button
<!-- To disable back button start-->
<script type="text/javascript">
history.pushState(null, null, location.href);
    window.onpopstate = function () {
        history.go(1);
    };
</script>
<!-- To disable back button end -->
<!-- To disable F5 button start -->
<script type="text/javascript">
document.onkeydown = function() {
    if(event.keyCode == 116) {
            event.returnValue = false;
            event.keyCode = 0;
            return false;
           }
}
</script>
<!-- To disable F5 button end -->
