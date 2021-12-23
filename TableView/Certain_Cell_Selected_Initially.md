      func tableView(_ tableView: UITableView, willDisplay cell: UITableViewCell, forRowAt indexPath: IndexPath) {
        if shouldSelectThisRow {
        tableView.selectRow(at: indexPath, animated: false, scrollPosition: .none)
      } else {
          tableView.deselectRow(at: indexPath, animated: false)
        }
      }
      
My code example:
![image](https://user-images.githubusercontent.com/81428296/147297016-8d177b04-5ef9-4301-9f44-d6f076e3db9e.png)
