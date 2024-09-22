

<h3>Colors</h3>

<h5>Link Colors</h5>


<p>You can change the default colors of links</p>

<a href="html_images.asp" target="_blank">HTML Images</a> 


<h1>Colcd</h1>

<h2>Lindlors</h2>


<p>You can change the default colors of links</p>

<a href="html_images.asp" target="_blank">HTML Images</a> 

<h1>Cogdfrs</h1>

<h2>Lindfgolors</h2>


<p>You can change the default colors of links</p>

<a href="https://www.youtube.com/watch?v=JvAxsWvqtbk" target="_blank">VIDEO</a> 

<script>
var answers = ["A", "C", "B"],
    tot = answers.length;
function getCheckedValue(radioName) {
    var radios = document.getElementsByName(radioName);
    for (var y = 0; y < radios.length; y++)
        if (radios[y].checked) return radios[y].value;
}
function getScore() {
    var score = 0;
    for (var i = 0; i < tot; i++)
        if (getCheckedValue("question" + i) === answers[i]) score += 1;
    return score;
}
function returnScore() {
    document.getElementById("myresults").innerHTML =
        "You got " + getScore() + "/" + tot;
    if (getScore() > 2) {
        console.log("Bravo");
    }
}

</script>


<ul class="quiz">
    <li>
        <h4>How?</h4>
        <ul class="choices">
            <li>
                <label
                    ><input type="radio" name="question0" value="A" /><span
                        >one</span
                    ></label
                >
            </li>
            <li>
                <label
                    ><input type="radio" name="question0" value="B" /><span
                        >two</span
                    ></label
                >
            </li>
            <li>
                <label
                    ><input type="radio" name="question0" value="C" /><span
                        >three</span
                    ></label
                >
            </li>
            <li>
                <label
                    ><input type="radio" name="question0" value="D" /><span
                        >four</span
                    ></label
                >
            </li>
        </ul>
    </li>
    
    
</ul>
<button class="view-results" onclick="returnScore()">See Grade</button>
<span id="myresults" class="my-results">Results</span>
