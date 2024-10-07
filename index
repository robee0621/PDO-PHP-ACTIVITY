<?php 
// Load database configuration
require_once 'core/dbConfig.php'; 
?>

<!DOCTYPE html>
<html lang="en">
<head>
	<!-- Character set and viewport settings -->
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>DATA OBJECTS PDO ACTIVITY</title>
	<!-- Basic styling for the table -->
	<style>
		table {
			width: 100%;
			border-collapse: collapse;
		}
		th, td {
			border: 1px solid #ddd;
			padding: 8px;
		}
		th {
			background-color: #f2f2f2;
		}
	</style>
</head>
<body>
	
    <?php  
	// SQL query to select all users
	$query = "SELECT * FROM Users";

    // Prepare the SQL statement
    $stmt = $pdo->prepare($query);

    // Execute the statement
    $stmt->execute();

    // Fetch all results
    $users = $stmt->fetchAll();

    // Check if there are any results
    if ($users) {
        // Start the HTML table
        echo "<table>";
        echo "<tr>
                <th>UserID</th>
                <th>Username</th>
                <th>First Name</th>
                <th>Last Name</th>
                <th>Date of Birth</th>
                <th>Password</th>
                <th>Date Added</th>
              </tr>";
        
        // Loop through the results and create a row for each user
        foreach ($users as $user) {
            echo "<tr>
                    <td>{$user['UserID']}</td>
                    <td>{$user['Username']}</td>
                    <td>{$user['FirstName']}</td>
                    <td>{$user['LastName']}</td>
                    <td>{$user['DateOfBirth']}</td>
                    <td>{$user['Password']}</td>
                    <td>{$user['DateAdded']}</td>
                  </tr>";
        }

        // End the HTML table
        echo "</table>";
    } else {
        echo "No records found.";
    }
    ?>

</body>
</html>
