use get_auth func for eligibility

--------------------------------------
# tasks
- [ ] make data for upwards/cashe/others
- [ ] check cashe for problems
- [ ] myaccount should show all transactions
- [ ] myaccount should continue user journey
- [ ] reponsive 
- [ ] eligiblity only once (boolean)
- [ ] myprofile full data
- [ ] autofilling (concept maybe)
- [ ] filter for lenders
------------------------------
# tasks hirrin
- [ ] sorting
- [ ] apply to post
- [ ] new post only admin
- [ ] apply page,
https://www.crescendo-global.com/jobs?utm_campaign=LN&utm_medium=CGLNP&utm_source=LNCG

https://www.crescendo-global.com/job/specialist-slash-senior-specialist-investment-strategy-2-plus-years?utm_campaign=LN&utm_medium=CGLNP&utm_source=LNCG

https://www.crescendo-global.com/job/specialist-slash-senior-specialist-investment-strategy-2-plus-years/apply?utm_campaign=LN&utm_medium=CGLNP&utm_source=LNCG
tooltip code remove
```jsx
                      <TooltipProvider>
                        <Tooltip>
                          <TooltipTrigger asChild>
                            <Button className="mb-[-10px] mt-4 px-0" variant="link">
                              By {post.author}
                            </Button>
                          </TooltipTrigger>
                          <TooltipContent>
                            <p>{post.authorEmail}</p>
                          </TooltipContent>
                        </Tooltip>
                      </TooltipProvider>
                      <small className="font-medium text-gray-700">
                        {new Date(post.createdAt).toLocaleDateString("en-US", {
                          year: "numeric",
                          month: "long",
                          day: "numeric",
                        })}
                      </small>


```