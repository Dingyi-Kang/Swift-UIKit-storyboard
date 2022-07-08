Official doc: https://developer.apple.com/documentation/uikit/views_and_controls/table_views/adding_headers_and_footers_to_table_sections

### 1. if you just wanna have a title, you can use this api
<img width="971" alt="image" src="https://user-images.githubusercontent.com/81428296/178077552-74e738e4-64d8-4a5f-97ed-74c4b2a2a776.png">

### 2. if you wanna configure other properties of the default headerFooterView in addition to title, you register the default headerFooter view in tableView and configure it in the HeaderViewForSection API
    self.tableView.register(UITableViewHeaderFooterView.self, forHeaderFooterViewReuseIdentifier:"header")
<img width="977" alt="image" src="https://user-images.githubusercontent.com/81428296/178077834-95926bca-f840-4ceb-9e09-e2255a2b9d09.png">

### you can configure the insets of header/footer via builder interface like below
#### note1: this is in the tableView
<img width="958" alt="image" src="https://user-images.githubusercontent.com/81428296/178077993-9a66d644-a3b4-488b-97b1-c50c4af58cc1.png">

#### in contrast, if want to set the seperators inset between cells within sections, you need to select cell and do like below, switch the seperator inset to custom. do similar for cell2
<img width="940" alt="image" src="https://user-images.githubusercontent.com/81428296/178078142-d3d58ff8-c1c8-41e0-966a-754e1a1fdb25.png">

#### note2: however, the seperator inset between header and cells will go along with the inset of header, like below
<img width="393" alt="image" src="https://user-images.githubusercontent.com/81428296/178078428-24ce4f80-0016-41ea-9b76-84e585a53c43.png">

#### If you wanna the seperaotr inset match with those between cell, do below:
<img width="532" alt="image" src="https://user-images.githubusercontent.com/81428296/178078475-3ba33ca3-75fa-4241-bfb0-7cfc7f75746c.png">

#### code:
    cell.layoutMargins = UIEdgeInsets.zero
    cell.preservesSuperviewLayoutMargins = false
### 3. it is also good to organize the source data in a 2d array as the indexPath struct
<img width="965" alt="image" src="https://user-images.githubusercontent.com/81428296/178078605-1c128edc-0d4c-40a3-adda-b462185a0433.png">
<img width="844" alt="image" src="https://user-images.githubusercontent.com/81428296/178078623-24a9ebc6-577c-41ae-82c3-01e98c69bef9.png">

### 4. lastly, if you wanna to have a more customized header, create a subclass of headerFootView, and register it in table with id (note when register, you register it as headfooterView instead tableViewCell. Or, you get a type error), and access it with id and case it to your custom class type
      class CustomHeader: UITableViewHeaderFooterView {
      let title = UILabel()

      override init(reuseIdentifier: String?) {
          super.init(reuseIdentifier: reuseIdentifier)
          configureContents()
      }

      required init?(coder: NSCoder) {
          fatalError("init(coder:) has not been implemented")
      }

      func configureContents() {
          title.translatesAutoresizingMaskIntoConstraints = false
          contentView.addSubview(title)

          NSLayoutConstraint.activate([
              // Center the label vertically
              title.heightAnchor.constraint(equalToConstant: 30),
              title.leadingAnchor.constraint(equalTo: contentView.layoutMarginsGuide.leadingAnchor,
                     constant: 8),
              title.centerYAnchor.constraint(equalTo: contentView.centerYAnchor)
          ])
      }
     }
  
 More details seen in the official doc
