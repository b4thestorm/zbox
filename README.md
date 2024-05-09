ZRO is built with the intention of stream lining the soft deletion of emails from Gmail. Built to scale the mass deletion
of unwanted emails. 

<div align="center">
        <img src="./media/deleteEmailSequence.png" width="450" height="400" alt="UML">
</div>

<h3><strong> API Contract</strong></h3>
<p>Home#activateJob - Activate asynchronous Celery process to begin queuing emails</p>
<p>Queue Service/fetchPage - Call Google to get page email ids</p>
<p>Queue Service/queuePage - Store email ids in Redis Queue </p>
<p>Queue Service/deleteEmail - Call Google to delete email </p>
<p>Queue Service/saveId - Store processed email ids in Redis cache </p>

<h3><strong>System Diagram</strong></h3>
<div align="center">
        <img src="./media/ZROSystemDiagram.png" width="400" height="400" alt="UML">
</div>