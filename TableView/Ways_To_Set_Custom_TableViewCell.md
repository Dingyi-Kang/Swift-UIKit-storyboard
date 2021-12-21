1. directly set identifier in the prototype cell in StoryBoard

![image](https://user-images.githubusercontent.com/81428296/146854096-19ebe36b-3aff-412f-bf76-bc9b507a4b73.png)

Then

    func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
    let cell = tableView.dequeueReusableCell(withIdentifier: "options")!
    return cell}
2. Create a nib and Register the custom cell(nib) in the tableView. (If cannot directly set identifier for custom cell in storyBoard (for example because too many types of custome cells))

        let nib = UINib(nibName: SectionTableViewCell.cellName, bundle: Bundle.main)
        tableView.register(nib, forCellReuseIdentifier: SectionTableViewCell.cellName)
        
   ![image](https://user-images.githubusercontent.com/81428296/146854791-793a2cb1-7503-42e1-bab3-b9422bcff552.png)
