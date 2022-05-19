# BlockChanger
1.7 - 1.18 utility class that allows you to change blocks at blazing fast speeds  

### Setup
Just import the class to your project.  
### Usage
```java
Player player = ...
BlockChanger.setBlock(player.getLocation(), Material.GOLD_BLOCK);
BlockChanger.setBlock(player.getLocation(), new ItemStack(Material.GOLD_BLOCK));
// Use async methods
// corner1 and corner2 are locations ofc.
BlockChanger.setCuboidAsynchronously(corner1, corner2, new ItemStack(Material.DIAMOND_BLOCK), false).thenRun(() -> {
	// gets executed after cuboid has been filled entirely
	Bukkit.broadcastMessage("COMPLETED!");
});
// Fastest method (setSection)
BlockChanger.setSectionCuboidAsynchronously(corner1, corner2, new ItemStack(Material.GLASS), false).thenRunAsync(() -> {
	Bukkit.broadcastMessage("COMPLETED!");
});
BlockChanger. // see all the methods
```  
### ToDo  
- Method to update lighting?  
