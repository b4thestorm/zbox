ZRO is built with the intention of stream lining the soft deletion of emails from Gmail. Built to scale the mass deletion
of unwanted emails. 
<br>
<br>
<h3><strong>System Diagram</strong></h3>
<div align="center">
        <img src="./media/SystemInboxZero.png" width="400" height="400" alt="UML">
</div>

<br>
<br>
<h3><strong> API </strong></h3>
<p><em>Index.activateJob</em>: Activate asynchronous Celery process to begin queuing emails</p>
<p><em>Queue Service/fetchPage</em>: Call Google to get page email ids</p>
<p><em>Queue Service/queuePage</em>: Store email ids in Redis Queue </p>
<p><em>Queue Service/deleteEmail</em>: Call Google to delete email </p>
<p><em>Queue Service/saveId</em>: Store processed email ids in Redis cache </p>

<br>
<br>
<h3><strong> Delete Sequence </strong></h3>
<div align="center">
        <img src="./media/deleteEmailSequence.png" width="450" height="400" alt="UML">
</div>