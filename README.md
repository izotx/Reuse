Reuse
=====

Reuse Repository  a collection of reusable macros and useful classes that you can use in every project.
Currently contains:
Macros.h - collection of macros
AppManager - Singleton
DataSource - a reusable data source for UITableView

Just drop the classes to your project to save yourself time.

If you want to use reusable data source you need to create an instance of DataSource using method below. 

NSArray * menuItems=@[@"Summit 2013",@"Sponsors",@"Agenda",@"Survey",@"About App"];
datasource = [[DataSource alloc]initWithItems:menuItems cellIdentifier:kCellId configureCellBlock:^(id cell, id item, id indexPath){
        [[(UITableViewCell *)cell textLabel] setText:[menuItems objectAtIndex:[(NSIndexPath *)indexPath row]]];
        
        
    }];
    self.tableView.dataSource = datasource;


