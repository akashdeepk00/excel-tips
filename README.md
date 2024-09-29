# excel-tips
All best Excel practices
<h1>Turning 12-Digit Phone Numbers into 10-Digit Numbers</h1>
<p>This formula converts 12-digit Indian phone numbers to a 10-digit format, removing extra spaces and non-printable characters.</p>
<p>=CLEAN(TRIM(IF(LEFT(P2,2)="91",IF(LEN(P2)=12,RIGHT(P2,10),P2),P2)))</p>

<h1>Calculating Age from DOB</h1>
<p>This formula calculates age in years based on the date of birth in cell F2.</p>
<p>=INT(YEARFRAC(TODAY(),F2,1))</p>

<h1>INDEX and MATCH Formula</h1>
<p>This formula retrieves a value from a range based on a matching criterion.</p>
<p>=INDEX($B$16:$B$27,MATCH(B7,$C$16:$C$27,0))</p>
<aside>
    <p>👉🏻 <strong>Where</strong>: </p>
    <p><strong>`$B$16:$B$27`</strong> is the list that contains the value we wish to return, the <strong>CustName</strong> column.</p>
    <p><strong>`MATCH(B7,$C$16:$C$27,0)`</strong> determines the row for the INDEX function Where:</p>
    <p><strong>`B7`</strong> is the value we are trying to find, our <strong>CustID</strong>.</p>
    <p><strong>`$C$16:$C$27`</strong> is where we are looking, the <strong>CustID</strong> column.</p>
    <p><strong>`0`</strong> means exact match.</p>
</aside>
<h1>Formula to split text at character</h1>
<p>=LEFT(text,FIND(character,text)-1)</p>
<p>=RIGHT(B5,LEN(B5)-FIND("_",B5))</p>
