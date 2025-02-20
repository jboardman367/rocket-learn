# rocket-learn
RLGym training tool

## TODO
- Add logging (✔ wandb only)
  - Give both PPO and RolloutGenerator access ✔
  - Also normal logging instead of prints
- Add reward normalization (and distribution?)
- Centralize RewardFunction ✔
- Transfer model to CPU before storing
- Model freedom
  - Multiple inputs ✔ (when obs is tuple it batches them one by one)
  - Allow shared layers
  - Recurrent?
  - Continuous actions if we really want
- Redis features 
  - Saving and loading ✔ (could be more streamlined though)
  - Full setup (architecture, params, config?) communicated via redis, can start worker with only IP (may not be feasible)
  - Version quality is most important measurement, need to log it ✔
  - Implement quality update ✔
- Long-term plan is to set up a stream and let (at least some) people contribute with rollouts
  - Keep track of who is contributing ✔, make on-screen leaderboards
  - Exact setup in [different repo](https://github.com/Rolv-Arild/Necto)
  - Rolv can keep it running on current PC, planning to get new one
  - Need to come to agreement on config (architecture, reward func, parameters etc.)
- Known issues
  - Sometimes very short episodes appear (<10 frames), seemingly without any reason
  - TrueSkill does not update
