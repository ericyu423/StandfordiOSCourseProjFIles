# Twitter Lecture Project essential steps


#  Use a framework. 

  1. create a project normally
  2. close the project
  3. create a work space
        * Just like how it work when you you cocopods to import a framework such as adMob, or FacebookLogin
        * It creates a single file name "work place"
        * default is created inside your "parent" project, however in this lecture the workplace file is put outside the proj
        * when you create by pods everything is do for you, but to do this manually there are 3 addition steps
  4. drag the project file "the single file" not the folder to the workplace now the file structure will show up 
  5. drag the framework project file
  6. inside workspace go to your project file -> embeded Binaries -> drag the toolbox looking icon into the binaries
  7. import Twitter (the frame work name)
  
  now is ready to be used
  
  bug.
  
  8. seem like the framework is out of date, after some search online, the way to solve it is to update to swift 3.0 syntax
  9. menu -> edit -> covert -> swift syntax (highlight the whole twistter folder) it will show u a tool box to select
  10. user.swift line 43. change var asPropertyList: AnyObject ---->    var asPropertyList: [String: Any]
  11. (make sure twitter framework is drag to embeded binaries)



#  Multi-thread example

         private func searchForTweets() {
                if let request = twitterRequest() {
                    lastTwitterRequest = request
                    request.fetchTweets{ [weak self] newTweets in
                       if request == self?.lastTwitterRequest {
                        DispatchQueue.main.async {
                            self?.tweets.insert(newTweets, at:0)
                            self?.tableView.insertSections([0], with: .fade)
                        }
                        }
                    }
                }
            }
 note 1: twitterRequest execution is not in the mainquque, because it have to wait for the fetch result
 
 note 2. tableView.insertSection is an UI update, all UI update should happen in mainqueue there for
 
 note 3. put the UI update call insiide Dispatch main queue 
 
